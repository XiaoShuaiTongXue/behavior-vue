<template>
  <!--线上行为检测-->
  <div class="content" id="online_behaviorPage">
    <div class="container-fluid p-0">
      <br>
      <br>
      <h1 class="h3 mb-3">线上行为检测</h1>

      <div class="row">

        <div class="col-12 col-lg-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">检测提示</h5>
              <h6 class="card-subtitle text-muted">正式上课后，老师可发起行为检测通知。</h6>
            </div>
            <div class="card-body">
              <div class="mb-3">
                <div class="alert alert-success alert-dismissible" role="alert">
                  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                  </button>
                  <div class="alert-icon">
                    <i class="far fa-fw fa-bell"></i>
                  </div>
                  <div class="alert-message">
                    <strong>开始检测通知已发送！</strong> 请老师提醒学生尽快开启摄像头。
                  </div>
                </div>
                <div class="alert alert-primary alert-dismissible" role="alert">
                  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                  </button>
                  <div class="alert-icon">
                    <i class="far fa-fw fa-bell"></i>
                  </div>
                  <div class="alert-message">
                    <strong>结束检测通知已发送！</strong> 请老师提醒学生课后关闭摄像头。
                  </div>
                </div>
                <div class="alert alert-secondary alert-dismissible" role="alert">
                  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                  </button>
                  <div class="alert-icon">
                    <i class="far fa-fw fa-bell"></i>
                  </div>
                  <div class="alert-message">
                    <strong>通知发送失败！</strong> 若是技术或网络问题请及时向管理员反馈！
                  </div>
                </div>
                <div class="card-body text-center">
                  <div class="mb-3">
                    <button class="btn btn-pill btn-primary">开始检测</button>
                    <button class="btn btn-pill btn-warning">结束检测</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-lg-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">班级行为检测分析</h5>
              <h6 class="card-subtitle text-muted">该功能将会针对课堂表现，实时生成班级分析报告。</h6>
            </div>
            <div class="card-body">
              <div class="chart chart-sm">
                <canvas id="chartjs-doughnut_online_class"></canvas>
              </div>
            </div>

          </div>
        </div>

        <div class="col-12 col-lg-6">
          <div class="card flex-fill w-100">
            <div class="card-header">
              <h5 class="card-title">课堂情况趋势图</h5>
              <h6 class="card-subtitle text-muted">通过人工智能分析，自动评估学生课堂总体表现。</h6>
            </div>
            <div class="card-body">
              <div class="chart">
                <canvas id="chartjs-line_online_class"></canvas>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-xl-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">课堂总体情况</h5>
              <h6 class="card-subtitle text-muted">包含课堂总人数、整体参与度、认真度等数据分析。 <code>日期</code></h6>
            </div>
            <table class="table table-striped">
              <thead>
              <tr>
                <th style="width:75%;">数据分析</th>
                <th>参数</th>
              </tr>
              </thead>
              <tbody>
              <tr>
                <td>课堂总人数：</td>
                <td>18</td>
              </tr>
              <tr>
                <td>整体参与度：</td>
                <td>0.5</td>
              </tr>
              <tr>
                <td>整体认真度：</td>
                <td>0.6</td>
              </tr>
              <tr>
                <td>观测开始时间：</td>
                <td>21：53:13</td>
              </tr>
              <tr>
                <td>观测总时长：</td>
                <td>89</td>
              </tr>
              </tbody>
            </table>
          </div>
        </div>

        <div class="col-12 col-lg-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">学生总体情况扇形图</h5>
              <h6 class="card-subtitle text-muted">具体分析每一位学生的行为状态，判断行为占比。</h6>
            </div>
            <div class="card-body">
              <div class="chart chart-sm">
                <canvas id="chartjs-pie_online_class"></canvas>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-xl-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">学生总体情况</h5>
              <h6 class="card-subtitle text-muted">包含书写总人次数、玩手机总人次数、传递纸条总人次数等数据分析。 <code>日期</code>
              </h6>
            </div>
            <table class="table table-striped">
              <thead>
              <tr>
                <th style="width:75%;">线上行为检测数据分析</th>
                <th>参数</th>
              </tr>
              </thead>
              <tbody>
              <tr>
                <td>线上听课总人次数：</td>
                <td>暂无</td>
              </tr>
              <tr>
                <td>线上说话总人次数：</td>
                <td>暂无</td>
              </tr>
              <tr>
                <td>线上旷课总人次数：</td>
                <td>暂无</td>
              </tr>
              </tbody>
            </table>
          </div>
        </div>

        <div class="col-12 col-lg-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">学生个人行为扇形图</h5>
              <h6 class="card-subtitle text-muted">具体分析单个学生的行为状态，判断行为占比。</h6>
              <br>
              <div class="form-group row">
                <label class="col-form-label col-sm-2 text-sm-right">搜索：</label>
                <div class="col-sm-10">
                  <input type="email" class="form-control" placeholder="请输入学号">
                </div>
              </div>
            </div>

            <div class="card-body">
              <div class="chart chart-sm">
                <canvas id="chartjs-doughnut_online_students"></canvas>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-xl-6">
          <div class="card">
            <div class="card-header">
              <h5 class="card-title">学生单个情况</h5>
              <h6 class="card-subtitle text-muted">该功能将会针对单个学生的课堂表现，生成个人的分析报告。 <code>日期</code></h6>
            </div>
            <table class="table table-striped">
              <thead>
              <tr>
                <th style="width:75%;">数据分析</th>
                <th>参数</th>
              </tr>
              </thead>
              <tbody>
              <tr>
                <td>个人参与度：</td>
                <td>0.6</td>
              </tr>
              <tr>
                <td>个人认真度：</td>
                <td>0.8</td>
              </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>
<script>
</script>
<style>
</style>
