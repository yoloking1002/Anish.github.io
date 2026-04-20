<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Recordati S.p.A. — Co-Investment Opportunity</title>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
:root{
  --navy:#0D1B3E;--nmid:#1A2F5A;--nlit:#243F78;
  --gold:#B8964E;--cream:#F8F6F1;--white:#FFFFFF;
  --g100:#F2F2F0;--g200:#E2E2DE;--g400:#A8A89E;--g600:#6C6C64;--g800:#3A3A34;
  --text:#1A1A18;--green:#1B5E42;--gl:#E8F2ED;--teal:#1A4A5A;--teall:#E6F0F4;
  --red:#B03030;--redl:#FDEAEA;
  --hh:110px;--tbh:50px;--top:160px;
}
*{box-sizing:border-box;margin:0;padding:0}
html{font-size:16px}
body{font-family:'DM Sans',sans-serif;font-weight:400;color:var(--text);background:var(--cream);line-height:1.7}
h1,h2,h3,h4{font-family:'EB Garamond',serif;font-weight:500;line-height:1.25}
#hdr{position:fixed;top:0;left:0;right:0;z-index:200;background:var(--navy);border-bottom:1px solid rgba(184,150,78,.25)}
.htop{display:flex;align-items:center;justify-content:space-between;padding:0 40px;height:var(--hh);gap:32px}
.brand{font-family:'EB Garamond',serif;font-size:20px;font-weight:500;color:var(--white);white-space:nowrap}
.brand span{color:var(--gold)}
.hkpis{display:flex;gap:1px;flex:1;max-width:840px;background:rgba(255,255,255,.08);border-radius:4px;overflow:hidden}
.hk{flex:1;padding:12px 14px;background:rgba(13,27,62,.6)}
.hkv{font-family:'EB Garamond',serif;font-size:18px;color:var(--white);line-height:1;margin-bottom:3px}
.hkv.g{color:var(--gold)}
.hkl{font-size:9.5px;color:rgba(255,255,255,.4);letter-spacing:.06em;text-transform:uppercase}
.cbadge{font-size:10px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;color:var(--gold);border:1px solid rgba(184,150,78,.35);padding:5px 12px;border-radius:2px;white-space:nowrap}
#tabs{display:flex;align-items:stretch;border-top:1px solid rgba(255,255,255,.06);height:var(--tbh);overflow-x:auto;scrollbar-width:none}
#tabs::-webkit-scrollbar{display:none}
.tb{flex-shrink:0;padding:0 17px;font-size:11px;font-weight:400;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.5);background:transparent;border:none;cursor:pointer;border-bottom:2px solid transparent;transition:color .18s,border-color .18s;white-space:nowrap}
.tb:hover{color:rgba(255,255,255,.85)}
.tb.on{color:var(--gold);border-bottom-color:var(--gold)}
#body{padding-top:var(--top);min-height:100vh}
.panel{display:none}
.panel.on{display:block}
.pi{max-width:1140px;margin:0 auto;padding:48px 48px 72px}
.ey{font-size:10.5px;font-weight:500;letter-spacing:.14em;text-transform:uppercase;color:var(--gold);margin-bottom:9px}
.st{font-size:34px;color:var(--navy);margin-bottom:7px}
.ss{font-size:15px;color:var(--g600);margin-bottom:30px;max-width:720px;line-height:1.65}
.dv{width:36px;height:2px;background:var(--gold);margin-bottom:24px}
/* THESIS CARDS */
.tgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.tc{background:var(--white);border:1px solid var(--g200);border-top:3px solid var(--gold);border-radius:6px;padding:22px 20px;transition:box-shadow .2s}
.tc:hover{box-shadow:0 6px 24px rgba(0,0,0,.07)}
.tn{font-family:'EB Garamond',serif;font-size:34px;color:var(--g200);line-height:1;margin-bottom:8px}
.tc h3{font-size:14.5px;color:var(--navy);margin-bottom:6px}
.tc p{font-size:12.5px;color:var(--g600);line-height:1.6}
/* KPI ROW */
.kr{display:grid;grid-template-columns:repeat(5,1fr);gap:1px;background:var(--g200);border:1px solid var(--g200);border-radius:6px;overflow:hidden;margin-bottom:30px}
.kp{background:var(--white);padding:18px 16px}
.kv{font-family:'EB Garamond',serif;font-size:24px;color:var(--navy);line-height:1;margin-bottom:3px}
.kd{font-size:11.5px;color:var(--green);font-weight:500;margin-bottom:3px}
.kl{font-size:11px;color:var(--g600)}
/* CHARTS */
.cgrid{display:grid;grid-template-columns:1fr 1fr;gap:22px}
.cc{background:var(--white);border:1px solid var(--g200);border-radius:6px;padding:20px}
.ct{font-family:'EB Garamond',serif;font-size:17px;color:var(--navy);margin-bottom:2px}
.cs{font-size:11px;color:var(--g400);margin-bottom:13px}
.cw{position:relative;height:205px}
.leg{display:flex;gap:14px;margin-top:9px;font-size:11px;color:var(--g600);flex-wrap:wrap}
.ld{width:9px;height:9px;border-radius:2px;display:inline-block;flex-shrink:0}
.ll{width:16px;height:2px;display:inline-block;flex-shrink:0;margin-bottom:2px;vertical-align:middle}
/* GUIDANCE CARDS */
.gg{display:grid;grid-template-columns:repeat(3,1fr);gap:13px;margin-top:18px}
.gg4{display:grid;grid-template-columns:repeat(4,1fr);gap:13px;margin-top:18px}
.gc{background:var(--g100);padding:15px 14px;border-radius:6px}
.gcl{font-size:10.5px;color:var(--g600);letter-spacing:.07em;text-transform:uppercase;margin-bottom:5px}
.gcv{font-family:'EB Garamond',serif;font-size:19px;color:var(--navy)}
.gcn{font-size:11px;color:var(--green);margin-top:3px}
/* CAP TABLE */
.capw{display:grid;grid-template-columns:1fr 1.2fr;gap:40px;align-items:start}
.capch{position:relative;height:280px}
.capleg{margin-top:13px;display:flex;flex-direction:column;gap:8px}
.capn{margin-top:14px;padding:12px 14px;background:var(--teall);border-left:3px solid var(--teal);border-radius:4px}
.capnt{font-size:11.5px;font-weight:500;color:var(--teal);margin-bottom:3px}
.capnd{font-size:11.5px;color:var(--g600);line-height:1.6}
/* TABLES */
table.s{width:100%;border-collapse:collapse;font-size:12.5px}
table.s th{text-align:left;padding:8px 10px;font-size:10px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;color:var(--g600);border-bottom:2px solid var(--navy)}
table.s td{padding:8px 10px;border-bottom:1px solid var(--g200);color:var(--text);vertical-align:middle}
table.s tr:last-child td{border-bottom:none}
table.s tr.tr td{font-weight:600;color:var(--navy);border-top:2px solid var(--navy);background:var(--g100)}
.bx{display:inline-block;font-size:9px;font-weight:500;padding:2px 7px;border-radius:2px;letter-spacing:.05em;text-transform:uppercase}
.bl{background:var(--navy);color:#fff}.bc{background:var(--gl);color:var(--green)}.bf{background:var(--g100);color:var(--g600)}.bp{background:#FEF3E2;color:#9A5B0A}.bm{background:var(--gl);color:var(--green)}
/* DEAL */
.dgrid{display:grid;grid-template-columns:1fr 1.15fr;gap:32px;align-items:start}
.dsumm{background:var(--navy);border-radius:8px;padding:22px 20px;color:var(--white)}
.dst{font-family:'EB Garamond',serif;font-size:16px;color:var(--gold);margin-bottom:16px}
.dsr{display:flex;justify-content:space-between;align-items:center;padding:8px 0;border-bottom:1px solid rgba(255,255,255,.09);font-size:12.5px}
.dsr:last-child{border-bottom:none}
.dsl{color:rgba(255,255,255,.55)}
.dsv{font-weight:500;color:var(--white)}
.dsv.g{color:var(--gold)}.dsv.gr{color:#6BCFAA}
.steps{margin-top:18px;display:flex;flex-direction:column;gap:13px}
.step{display:flex;gap:11px;align-items:flex-start}
.sn{width:24px;height:24px;border-radius:50%;background:var(--navy);color:var(--gold);display:flex;align-items:center;justify-content:center;font-size:11.5px;font-weight:500;flex-shrink:0;margin-top:3px}
.step h4{font-size:13px;color:var(--navy);margin-bottom:2px}
.step p{font-size:12px;color:var(--g600)}
/* MARKET */
.mkpi{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--g200);border:1px solid var(--g200);border-radius:6px;overflow:hidden;margin-bottom:26px}
.mk{background:var(--navy);padding:17px 14px}
.mkl{font-size:9.5px;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.4);margin-bottom:6px}
.mkv{font-family:'EB Garamond',serif;font-size:23px;color:var(--white);line-height:1}
.mkn{font-size:10.5px;color:var(--gold);margin-top:4px}
/* DRUG TABLE */
.dtcard{background:var(--white);border:1px solid var(--g200);border-radius:6px;overflow:hidden;margin-top:14px}
.dtrow{display:grid;grid-template-columns:1fr 1fr 105px;border-bottom:1px solid var(--g200)}
.dtrow:last-child{border-bottom:none}
.dtrow>div{padding:8px 13px;font-size:12px}
.dtrow>div:first-child{font-weight:500;color:var(--navy);border-right:1px solid var(--g200)}
.dtrow>div:nth-child(2){color:var(--g600);border-right:1px solid var(--g200)}
.dtrow>div:last-child{display:flex;align-items:center;justify-content:center}
.dthdr{background:var(--g100);display:grid;grid-template-columns:1fr 1fr 105px}
.dthdr>span{padding:6px 13px;font-size:9.5px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;color:var(--g600);border-bottom:2px solid var(--navy)}
.dthdr>span:first-child,.dthdr>span:nth-child(2){border-right:1px solid var(--g200)}
/* CO-INVESTORS */
.ittl{font-size:11px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;color:var(--g400);margin:22px 0 10px;padding-bottom:6px;border-bottom:1px solid var(--g200)}
.ir{display:grid;grid-template-columns:180px 75px 1fr 80px;gap:12px;align-items:center;padding:10px 0;border-bottom:1px solid var(--g200);font-size:12px}
.ir:last-child{border-bottom:none}
.in{font-weight:500;color:var(--navy)}.it{font-size:10px;color:var(--g400);margin-top:2px}
.ia{font-size:12px;font-weight:500;color:var(--g800)}
.ino{font-size:11px;color:var(--g600);line-height:1.5}
.fp{display:inline-block;font-size:9.5px;font-weight:500;padding:3px 9px;border-radius:10px;text-transform:uppercase;letter-spacing:.05em}
.fs{background:var(--gl);color:var(--green)}.fm{background:#FEF3E2;color:#9A5B0A}
/* RETURNS */
.rgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-bottom:24px}
.sc{border:1px solid var(--g200);border-radius:8px;overflow:hidden}
.sch{padding:13px 17px;display:flex;justify-content:space-between;align-items:center}
.sch h3{font-size:16px;color:var(--white)}
.sct{font-size:10px;font-weight:500;letter-spacing:.06em;text-transform:uppercase;color:rgba(255,255,255,.65)}
.bear .sch{background:#3A2020}.base .sch{background:var(--navy)}.bull .sch{background:var(--green)}
.scb{padding:13px 17px}
.ss2{display:flex;justify-content:space-between;padding:6px 0;border-bottom:1px solid var(--g200);font-size:12px}
.ss2:last-child{border-bottom:none}
.ssl{color:var(--g600)}.ssv{font-weight:500;color:var(--navy)}
.ssv.hi{color:var(--green);font-family:'EB Garamond',serif;font-size:15px}
/* RISKS */
.rg{display:grid;grid-template-columns:1fr 1fr;gap:15px}
.rc{border:1px solid var(--g200);border-radius:6px;padding:17px;border-left:4px solid var(--g400)}
.rc.high{border-left-color:#C0392B}.rc.med{border-left-color:#E67E22}.rc.low{border-left-color:var(--green)}
.rh{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:7px}
.rt{font-family:'EB Garamond',serif;font-size:15.5px;color:var(--navy)}
.rl{font-size:9px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;padding:2px 7px;border-radius:2px}
.rhi{background:#FDEDEC;color:#C0392B}.rme{background:#FEF9E7;color:#9A5B0A}.rlo{background:var(--gl);color:var(--green)}
.rdesc{font-size:12px;color:var(--g600);line-height:1.6;margin-bottom:7px}
.rmit{font-size:11px;color:var(--teal);font-weight:500}
/* VALUATION DISCOUNT */
.vdgrid{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-bottom:24px}
.rc2{background:var(--white);border:1px solid var(--g200);border-radius:6px;padding:18px;border-left:4px solid var(--navy)}
.rc2.q{border-left-color:var(--gold)}
.rn{font-family:'EB Garamond',serif;font-size:26px;color:var(--g200);line-height:1;margin-bottom:5px}
.rtitle{font-size:14px;font-weight:500;color:var(--navy);margin-bottom:5px}
.rbody{font-size:12px;color:var(--g600);line-height:1.6}
.rtag{display:inline-block;margin-top:6px;font-size:11px;font-weight:500;color:var(--gold);background:#FBF6EC;padding:3px 8px;border-radius:3px}
.rfix{margin-top:6px;font-size:11px;color:var(--green);font-weight:500}
.aband{background:var(--navy);border-radius:8px;padding:20px 22px;color:var(--white);margin-bottom:22px}
.ab-title{font-family:'EB Garamond',serif;font-size:17px;color:var(--gold);margin-bottom:12px}
.abg{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(255,255,255,.1);border-radius:4px;overflow:hidden;margin-top:13px}
.abc{background:rgba(13,27,62,.6);padding:13px}
.abv{font-family:'EB Garamond',serif;font-size:19px;color:var(--white)}
.abv.g{color:var(--gold)}
.abl{font-size:9.5px;color:rgba(255,255,255,.45);letter-spacing:.06em;text-transform:uppercase;margin-top:3px}
/* Deal */
.lsrc{display:grid;grid-template-columns:1fr 1fr;gap:22px;margin-bottom:24px}
.lcard{background:var(--white);border:1px solid var(--g200);border-radius:6px;padding:20px}
.lt{font-family:'EB Garamond',serif;font-size:17px;color:var(--navy);margin-bottom:3px}
.ls{font-size:11px;color:var(--g400);margin-bottom:14px}
.lstack{display:flex;flex-direction:column;gap:2px;margin-bottom:12px}
.lbar{height:36px;display:flex;align-items:center;padding:0 13px;border-radius:3px;font-size:11.5px;font-weight:500;color:#fff;justify-content:space-between}
.dnote{font-size:10.5px;color:var(--g400);margin-top:7px;font-style:italic;border-top:1px solid var(--g200);padding-top:7px}
.cft{width:100%;border-collapse:collapse;font-size:12px}
.cft th{background:var(--navy);color:var(--white);padding:8px 9px;font-size:10px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;text-align:right}
.cft th:first-child{text-align:left}
.cft td{padding:7px 9px;border-bottom:1px solid var(--g200);text-align:right}
.cft td:first-child{text-align:left;color:var(--g600)}
.cft tr.sec td{background:var(--g100);font-weight:600;color:var(--navy);font-size:10px;letter-spacing:.06em;text-transform:uppercase}
.cft tr.tot td{background:var(--navy);color:var(--white);font-weight:600;border-top:none}
.cft tr.sub td{font-weight:600;color:var(--navy);background:#F8F8F5}
.cft tr.gr td{color:var(--green);font-weight:600}
.cft tr.re td{color:#C0392B;font-weight:600}
.cft tr.hl td{background:#EAF0FA;color:var(--navy);font-weight:600}
.stabs{display:flex;gap:7px;margin-bottom:14px}
.stab{padding:7px 15px;font-size:11.5px;font-weight:500;border-radius:4px;border:1px solid var(--g200);cursor:pointer;background:var(--white);color:var(--g600);transition:all .18s}
.stab.on{background:var(--navy);color:var(--white);border-color:var(--navy)}
.sp{display:none}
.sp.on{display:block}
.icrg{display:grid;grid-template-columns:repeat(5,1fr);gap:1px;background:var(--g200);border:1px solid var(--g200);border-radius:6px;overflow:hidden;margin-top:18px}
.icrc{background:var(--white);padding:14px 13px}
.icrv{font-family:'EB Garamond',serif;font-size:22px;color:var(--navy)}
.icrl{font-size:10px;color:var(--g600);margin-top:3px}
.icrc.ok .icrv{color:var(--green)}.icrc.warn .icrv{color:#C0392B}
/* SPACING */
.mt12{margin-top:12px}.mt16{margin-top:16px}.mt20{margin-top:20px}.mt24{margin-top:24px}.mt28{margin-top:28px}
/* FOOTER */
footer{background:var(--navy);padding:22px 48px;display:flex;justify-content:space-between;align-items:center;gap:40px}
.fb{font-family:'EB Garamond',serif;font-size:15px;color:var(--white);white-space:nowrap}
.fb span{color:var(--gold)}
.fd{font-size:10.5px;color:rgba(255,255,255,.3);max-width:660px;line-height:1.6}
@media(max-width:900px){
  .tgrid,.cgrid,.dgrid,.rg,.capw,.lsrc,.vdgrid{grid-template-columns:1fr}
  .kr,.mkpi,.abg,.icrg{grid-template-columns:repeat(2,1fr)}
  .ir{grid-template-columns:1fr 1fr}.rgrid{grid-template-columns:1fr}
  .hkpis{display:none}.pi{padding:30px 20px 56px}
}
</style>
</head>
<body>

<div id="hdr">
  <div class="htop">
    <div class="brand">Recordati <span>S.p.A.</span></div>
    <div class="hkpis">
      <div class="hk"><div class="hkv g">€12.24bn</div><div class="hkl">Enterprise Value (PitchBook)</div></div>
      <div class="hk"><div class="hkv">€10.20bn</div><div class="hkl">Equity Value (Market Cap)</div></div>
      <div class="hk"><div class="hkv">€52.00</div><div class="hkl">Offer Price per Share</div></div>
      <div class="hk"><div class="hkv g">€991M</div><div class="hkl">FY2025 EBITDA</div></div>
      <div class="hk"><div class="hkv">12.35×</div><div class="hkl">Entry EV/EBITDA</div></div>
      <div class="hk"><div class="hkv">37.8%</div><div class="hkl">EBITDA Margin</div></div>
    </div>
    <div class="cbadge">Confidential</div>
  </div>
  <div id="tabs">
    <button class="tb on" data-tab="thesis">Investment Thesis</button>
    <button class="tb" data-tab="valuation">Valuation Discount</button>
    <button class="tb" data-tab="financials">Financials</button>
    <button class="tb" data-tab="lbo">LBO Returns Model</button>
    <button class="tb" data-tab="captable">Cap Table</button>
    <button class="tb" data-tab="deal">Deal Structure</button>
    <button class="tb" data-tab="market">Market</button>
    <button class="tb" data-tab="coinvestors">Co-Investors</button>
    <button class="tb" data-tab="returns">Returns</button>
    <button class="tb" data-tab="ipo">SPC Exit</button>
    <button class="tb" data-tab="risks">Risk Factors</button>
  </div>
</div>

<div id="body">

<!-- THESIS ══════════════════════════════════════════════════════ -->
<div class="panel on" id="p-thesis">
<div class="pi">
  <div class="ey">Co-Investment Opportunity · April 2026</div>
  <h2 class="st">The Case for Recordati</h2>
  <div class="dv"></div>
  <p class="ss">CVC Capital Partners and its existing consortium are inviting select co-investors to participate in a cash tender offer for the 53.2% free float of Recordati S.p.A. at €52 per share. The transaction values the business at €12.24bn enterprise value (source: PitchBook, 17 April 2026), implying a 12.35× FY2025 EBITDA entry multiple, which is at a five-year low despite double-digit compounding growth, and creates a platform for one of the more compelling value creation stories in European healthcare private equity today.</p>
  <div class="tgrid">
    <div class="tc"><div class="tn">01</div><h3>Entry at a Five-Year Low</h3><p>Recordati trades at 12.35× EV/EBITDA, down from a peak of 21.8× in 2021 and well below its decade average premium to peers. That compression has occurred while EBITDA grew at 13.5% annually. Six structural headwinds are all well-documented and most directly removable through the take-private explain the gap. The market is pricing a conglomerate. Private ownership unlocks a rare disease platform worth materially more.</p></div>
    <div class="tc"><div class="tn">02</div><h3>Rare Disease Drugs at a Conglomerate Discount</h3><p>Recordati's rare disease division — growing revenue at 29.7% in FY2025 to €1,081M — is blended into a group multiple of 12.35× alongside a slower specialty pharma business growing at just 2%. Pure-play rare disease drug companies attract 18 to 22× EBITDA in M&A markets. The carve-out thesis separates these two businesses and captures that premium through a strategic sale of the rare disease division at the end of Year 3.</p></div>
    <div class="tc"><div class="tn">03</div><h3>A Co-Investment Structure with No Fees</h3><p>Incoming co-investors participate directly in the tender offer alongside CVC and the existing Rossini consortium. There is no fund layer, no management fee and no carried interest payable to an intermediary. Investors receive the same economics as the sponsor on the equity deployed to acquire the free float, where new co-investors contribute €2,131M in cash equity (covering their €2,110M share of the free float purchase plus €21M of transaction costs), and the Rossini consortium rolls €5,002M of existing equity, for a total of €7,133M of equity in the transaction.</p></div>
    <div class="tc"><div class="tn">04</div><h3>Specialty Pharma Funds the Whole Hold Period</h3><p>The specialty pharma business generates €559M in free cash flow annually. At a 5.0% interest rate on €5,982M of debt, annual interest in Years 1 to 3 is €299M. EBITDA coverage is 3.3× from day one — before any EBITDA growth — providing a comfortable buffer throughout the hold period while the rare disease division is prepared for a premium exit.</p></div>
    <div class="tc"><div class="tn">05</div><h3>Isturisa: A Platform Asset in Full Stride</h3><p>The FDA expanded Isturisa's label in April 2025 to cover all Cushing's syndrome patients, roughly doubling the addressable market. Management raised peak sales guidance above €1.2bn. The lead competitive drug, relacorilant, received a Complete Response Letter from the FDA in December 2025 for its Cushing's syndrome NDA, leaving Isturisa as the dominant medical treatment for Cushing's disease with a clear commercial runway. In March 2026, relacorilant was separately approved for platinum-resistant ovarian cancer under the brand name Lifyorli — a distinct indication that does not compete with Isturisa's endocrinology franchise. The rare disease division exit valuation is primarily anchored to this single asset.</p></div>
    <div class="tc"><div class="tn">06</div><h3>Sponsor Track Record Since 2018</h3><p>CVC has owned Recordati through the Rossini HoldCo since 2018 alongside PSP Investments, StepStone and AlpInvest. Management relationships are deep, the carve-out roadmap is understood and the rare disease division already operates as a standalone subsidiary with its own commercial infrastructure, logistics hub in Nanterre and separate reporting lines. There is no integration work to do, only value to extract.</p></div>
  </div>
</div>
</div>

<!-- VALUATION DISCOUNT ══════════════════════════════════════════ -->
<div class="panel" id="p-valuation">
<div class="pi">
  <div class="ey">Why the Market is Wrong</div>
  <h2 class="st">The Valuation Disconnect</h2>
  <div class="dv"></div>
  <p class="ss">Recordati earns a 37.8% EBITDA margin, grows at double digits and holds a rare disease drug portfolio that commands 18 to 22× multiples in comparable transactions. It trades at 12.35× because of six overlapping structural discounts, each well documented and most directly curable in private hands. Understanding this is the foundation of the entire investment thesis.</p>

  <div class="cc mt16" style="margin-bottom:22px;">
    <div class="ct">EV/EBITDA Multiple — Recordati vs European Pharma Peers (2020 to 2026)</div>
    <div class="cs">The stock has de-rated 44% from its 2021 peak of 21.8× to 12.35× today, a compression that has happened entirely while EBITDA compounded at 13.5% per year</div>
    <div class="cw" style="height:230px;"><canvas id="evChart"></canvas></div>
    <div class="leg mt16">
      <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#0D1B3E;"></span>Recordati EV/EBITDA</span>
      <span style="display:flex;align-items:center;gap:5px;"><span class="ll" style="background:#B8964E;"></span>European Pharma Peer Average</span>
      <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#C0392B;border-radius:50%;"></span>Current (12.35× — five-year low)</span>
    </div>
  </div>

  <div class="aband">
    <div class="ab-title">What the Analysts Are Saying</div>
    <p style="font-size:12.5px;color:rgba(255,255,255,.65);line-height:1.65;">Ten brokers cover Recordati. Kepler Cheuvreux upgraded to Buy in February 2026, writing that the stock now sits at a discount to European pharma peers — the reverse of the 20% premium it averaged over the prior decade. Barclays upgraded to Equal Weight noting the stock is inexpensive relative to its own history. The average twelve-month price target across ten analysts is €60.6, implying 21.2% upside to the 17 April 2026 close of €50.00. CVC's offer of €52 reflects just 4.0% above that close, meaning the consortium is acquiring the business at a meaningful discount to where the public market consensus sees intrinsic value.</p>
    <div class="abg">
      <div class="abc"><div class="abv g">€60.6</div><div class="abl">Analyst Consensus Target</div></div>
      <div class="abc"><div class="abv">10</div><div class="abl">Brokers Covering</div></div>
      <div class="abc"><div class="abv g">+24%</div><div class="abl">Upside vs Pre-Deal Price</div></div>
      <div class="abc"><div class="abv">9/10</div><div class="abl">Buy or Hold Ratings</div></div>
    </div>
  </div>

  <h3 style="font-family:'EB Garamond',serif;font-size:19px;color:var(--navy);margin-bottom:14px;">Six Structural Reasons for the Discount — and What Happens to Each Under Private Ownership</h3>
  <div class="vdgrid">
    <div class="rc2 q">
      <div class="rn">01</div>
      <div class="rtitle">The PE Ownership Overhang</div>
      <div class="rbody">CVC's 46.8% Rossini HoldCo stake is the single most cited reason for the discount, explicitly flagged by Kepler Cheuvreux as "a key concern and key overhang." Index funds cannot adequately weight the stock given the restricted free float. Long-only institutions avoid building positions in businesses where a PE owner might conduct a secondary sale at any time. This dynamic alone is responsible for an estimated two to three multiple-point discounts versus comparably positioned pharma companies with clean shareholder registers.</div>
      <div class="rtag">Estimated discount: 2 to 3× EBITDA</div>
      <div class="rfix">Take-private eliminates the overhang on day one</div>
    </div>
    <div class="rc2 q">
      <div class="rn">02</div>
      <div class="rtitle">The Conglomerate Blending Problem</div>
      <div class="rbody">The market prices Recordati as a single entity at 12.35× blended EBITDA. Its rare disease division growing at 30% deserves 18 to 22× on pure-play comparables. Its specialty pharma division, which is growing at 2%, deserves 9 to 11×. Academic research on conglomerate discounts in healthcare estimates a 10 to 20% valuation haircut for multi-segment operators versus pure-play peers. The sum-of-the-parts analysis places fair value up to €15.0bn, immediately above the €12.24bn entry EV in the base case and well above it in the bull case.</div>
      <div class="rtag">SOTP gap: €0 to €2.85bn above entry EV</div>
      <div class="rfix">Carve-out in Year 3 realises the pure-play rare disease premium</div>
    </div>
    <div class="rc2">
      <div class="rn">03</div>
      <div class="rtitle">Persistent Currency Drag</div>
      <div class="rbody">Approximately 20% of group revenue is denominated in US dollars and 2.5% in Turkish lira. FX movements reduced reported FY2025 revenue by €64.2M and are expected to reduce FY2026 revenue by a further 3.5%. Turkey faced 30% currency devaluation in 2025 with no offsetting price increases. The market penalises reported growth that runs below constant-currency growth, creating a systematic discount to underlying earnings quality that is unlikely to reverse quickly given macro conditions.</div>
      <div class="rtag">Confirmed drag: €64M on FY2025 revenue; 3.5% forecast for FY2026</div>
    </div>
    <div class="rc2">
      <div class="rn">04</div>
      <div class="rtitle">Specialty Pharma Maturation</div>
      <div class="rbody">The specialty pharma division grew 2.0% in FY2025, weighed down by the loss of the Cardicor licence (&#x20AC;35M/year from 2026) and generic competition for Carbaglu in the US and Europe. Core franchises include: Urology (Eligard, Urorec), Cardiovascular (Zanidip, Vazkepa licensed from Amarin in 2025), and Gastrointestinal, which remain intact and growing. However, the SPC business carries modest patent expiry risk on selected products through 2026 to 2030, and slower-than-expected new country entries could limit the geographic expansion thesis. Management guidance explicitly projects low single-digit SPC growth in FY2026. Investors are right to discount the division — but they apply that discount to the entire group, which is precisely where the pricing inefficiency lies.</div>
      <div class="rtag">SPC revenue growth: 2.0% in FY2025 vs 29.7% for Rare Disease</div>
    </div>
    <div class="rc2">
      <div class="rn">05</div>
      <div class="rtitle">The Italian Market Country Discount</div>
      <div class="rbody">Italian-listed companies trade at a systematic 10 to 15% discount to UK and Northern European peers. The STOXX 600 trades at approximately 11 to 12× EV/EBITDA on a blended basis. Concentrated ownership via Rossini Luxembourg, limited analyst coverage depth versus London peers, and Italy's higher sovereign risk premium all contribute to the discount. A US or UK-listed pure-play rare disease platform growing at Recordati's pace would typically command 15 to 18× EBITDA. The conglomerate discount — the cost of having two very different businesses under one roof is the largest single driver of the valuation gap.</div>
      <div class="rtag">Estimated country discount: 10 to 15% versus Northern European peers</div>
      <div class="rfix">Delisting from Borsa Italiana eliminates the listing venue discount entirely</div>
    </div>
    <div class="rc2">
      <div class="rn">06</div>
      <div class="rtitle">Near-Term Earnings Investment Cycle</div>
      <div class="rbody">Management has guided for €40M of incremental commercial spending in FY2026 to support the Isturisa label expansion into the broader Cushing's syndrome population. This caused Kepler Cheuvreux to trim 2026 EPS forecasts by 5%. A €14.1M one-off AIFA litigation provision also weighed on FY2025 net income. Investors are discounting near-term margin uncertainty without modelling the payback. Isturisa revenue is already accelerating, with approximately 1,400 net active US patients at year-end 2025 and uptake accelerating through the second half of the year.</div>
      <div class="rtag">Margin impact: 1.5 percentage points off FY2026 margin; temporary</div>
      <div class="rfix">Investment cycle ends in FY2027 as revenue ramp absorbs spend</div>
    </div>
  </div>

  <div style="background:var(--navy);border-radius:8px;padding:22px;margin-top:4px;">
    <div style="font-family:'EB Garamond',serif;font-size:17px;color:var(--gold);margin-bottom:10px;">The Investment Argument</div>
    <p style="font-size:13px;color:rgba(255,255,255,.72);line-height:1.75;">Recordati's 12.35× entry multiple is not a reflection of the quality of the underlying businesses. It is the product of six overlapping structural discounts, three of which — the PE ownership overhang, the Italian listing venue discount and the conglomerate blending problem — are directly eliminated by the take-private and subsequent rare disease division carve-out. The remaining three are cyclical or partially mitigated by Isturisa's commercial acceleration. The 44% de-rating from the 2021 peak has occurred entirely while EBITDA has compounded at 13.5% annually and margins have expanded every year. Private ownership removes the structural noise and allows the rare disease division to be monetised at the multiples it deserves.</p>
  </div>
</div>
</div>

<!-- FINANCIALS ══════════════════════════════════════════════════ -->
<div class="panel" id="p-financials">
<div class="pi">
  <div class="ey">Financial Performance</div>
  <h2 class="st">Compounding Margins, Growing Faster Than Guided</h2>
  <div class="dv"></div>
  <div class="kr">
    <div class="kp"><div class="kv">€2,618M</div><div class="kd">+11.8%</div><div class="kl">FY2025 Revenue</div></div>
    <div class="kp"><div class="kv">€991M</div><div class="kd">+14.5%</div><div class="kl">FY2025 EBITDA</div></div>
    <div class="kp"><div class="kv">37.8%</div><div class="kd">+90bps</div><div class="kl">EBITDA Margin</div></div>
    <div class="kp"><div class="kv">€559M</div><div class="kd">+8.2%</div><div class="kl">Free Cash Flow</div></div>
    <div class="kp"><div class="kv">2.1×</div><div class="kd">Pre-deal leverage</div><div class="kl">Net Debt / EBITDA</div></div>
  </div>
  <div class="cgrid">
    <div class="cc">
      <div class="ct">Revenue by Division</div>
      <div class="cs">FY2021 to FY2025 · €M · Rare Disease grew 29.7% in FY2025 against Specialty Pharma at 2.0%</div>
      <div class="cw"><canvas id="revChart"></canvas></div>
      <div class="leg mt16">
        <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#0D1B3E;"></span>Rare Disease</span>
        <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#B8964E;"></span>Specialty Pharma</span>
      </div>
    </div>
    <div class="cc">
      <div class="ct">EBITDA and Margin Expansion</div>
      <div class="cs">FY2021 to FY2025 · €M and % · Margin has expanded every year despite FX headwinds</div>
      <div class="cw"><canvas id="ebitdaChart"></canvas></div>
      <div class="leg mt16">
        <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#0D1B3E;"></span>EBITDA €M</span>
        <span style="display:flex;align-items:center;gap:5px;"><span class="ll" style="background:#B8964E;"></span>Margin %</span>
      </div>
    </div>
  </div>
  <div class="cc mt20">
    <div class="ct">Enterprise Value Bridge — PitchBook Verified (17 April 2026)</div>
    <div class="cs">Source: PitchBook, 17 April 2026. Gross debt €2.467bn (term loans €2.057bn + bonds/notes €321M + leases €49M). Cash €429M. Net debt = €2.039bn. Enterprise Value = €12.24bn.</div>
    <div class="gg4">
      <div class="gc"><div class="gcl">Equity Value (Market Cap)</div><div class="gcv">€10.20bn</div><div class="gcn">203.4M shares × €50.00</div></div>
      <div class="gc"><div class="gcl">Gross Debt</div><div class="gcv">€2.467bn</div><div class="gcn">PitchBook Q3 2025 — see Debt Instruments tab</div></div>
      <div class="gc"><div class="gcl">Cash and Equivalents</div><div class="gcv">(€429M)</div><div class="gcn">Net debt = €2.039bn (2.1× EBITDA)</div></div>
      <div class="gc"><div class="gcl">Enterprise Value</div><div class="gcv" style="color:var(--gold);">€12.24bn</div><div class="gcn">Entry EV/EBITDA: 12.35×</div></div>
    </div>
  </div>
  <div class="cc mt20">
    <div class="ct">FY2026 Management Guidance — Issued 17 February 2026</div>
    <div class="cs">Includes an FX headwind of approximately 3.5%. The incremental €40M Isturisa commercial investment is absorbed in these targets.</div>
    <div class="gg">
      <div class="gc"><div class="gcl">Revenue</div><div class="gcv">€2,730 to 2,800M</div><div class="gcn">+4.3% to +6.9% year on year</div></div>
      <div class="gc"><div class="gcl">EBITDA</div><div class="gcv">€995 to 1,030M</div><div class="gcn">Forward EV/EBITDA 11.8× at midpoint</div></div>
      <div class="gc"><div class="gcl">Adjusted Net Income</div><div class="gcv">€655 to 685M</div><div class="gcn">Margin approximately 24.0%</div></div>
    </div>
  </div>
</div>
</div>

<!-- Deal MODEL ══════════════════════════════════════════════════ -->
<div class="panel" id="p-lbo">
<div class="pi">
  <div class="ey">Financial Modelling</div>
  <h2 class="st">LBO Returns Model</h2>
  <div class="dv"></div>
  <p class="ss">This is a leveraged buyout. A consortium of new and existing co-investors acquires 100% of Recordati at a total transaction value of &#x20AC;13,115M, funded through &#x20AC;7,133M of equity and &#x20AC;5,982M of debt. The Rossini consortium rolls &#x20AC;4,953M of existing equity and contributes &#x20AC;49M toward transaction costs. New co-investors provide &#x20AC;2,110M to fund the free float purchase and &#x20AC;21M toward transaction costs, totalling &#x20AC;2,131M. Existing Recordati debt of &#x20AC;2,467M is refinanced and a new term loan of &#x20AC;3,515M is raised to fund the free float buyout, bringing total debt in the private entity to &#x20AC;5,982M at 5.0% interest. The rare disease division is sold in Year 3, with 50% of total group debt (&#x20AC;2,991M) repaid from proceeds. The residual specialty pharma entity exits via IPO or strategic sale in Year 5. All figures are illustrative estimates.</p>

  <!-- SOURCES USES + CAPITAL STRUCTURE -->
  <div class="lsrc">
    <div class="lcard">
      <div class="lt">Sources and Uses &#x2014; Total Transaction Value &#x20AC;13,115M</div>
      <div class="ls">Equity funds 54% of the deal. Debt funds 46%. Transaction costs of &#x20AC;70M are split 30% to new co-investors and 70% to existing co-investors.</div>
      <table class="s">
        <thead><tr><th>Sources</th><th style="text-align:right">&#x20AC;M</th><th style="text-align:right">% of Total</th></tr></thead>
        <tbody>
          <tr><td>New co-investor equity (&#x20AC;2,110M free float + &#x20AC;21M transaction costs)</td><td style="text-align:right">2,131</td><td style="text-align:right">16%</td></tr>
          <tr><td>Existing co-investors &#x2014; Rossini rollover (&#x20AC;4,953M + &#x20AC;49M transaction costs)</td><td style="text-align:right">5,002</td><td style="text-align:right">38%</td></tr>
          <tr><td>Existing Recordati debt refinanced</td><td style="text-align:right">2,467</td><td style="text-align:right">19%</td></tr>
          <tr><td>New term loan (funds free float purchase)</td><td style="text-align:right">3,515</td><td style="text-align:right">27%</td></tr>
          <tr class="tr"><td>Total transaction value</td><td style="text-align:right">13,115</td><td style="text-align:right">100%</td></tr>
        </tbody>
      </table>
      <table class="s mt12">
        <thead><tr><th>Uses</th><th style="text-align:right">&#x20AC;M</th></tr></thead>
        <tbody>
          <tr><td>Cash to free float shareholders (203.4M shares &#xD7; &#x20AC;52)</td><td style="text-align:right">5,625</td></tr>
          <tr><td>Transaction costs</td><td style="text-align:right">70</td></tr>
          <tr><td>Refinance existing Recordati debt</td><td style="text-align:right">2,467</td></tr>
          <tr><td>Rossini equity rollover</td><td style="text-align:right">4,953</td></tr>
          <tr class="tr"><td>Total</td><td style="text-align:right">13,115</td></tr>
        </tbody>
      </table>
      <p style="font-size:10px;color:#A8A89E;margin-top:8px;font-style:italic;">New co-investors bear 30% of transaction costs (&#x20AC;21M). Existing co-investors bear 70% (&#x20AC;49M). Existing Recordati debt of &#x20AC;2,467M is fully refinanced. A new &#x20AC;3,515M term loan is layered on top to fund the free float buyout, bringing total entity debt to &#x20AC;5,982M. Entry EV/EBITDA: &#x20AC;13,115M &#xF7; &#x20AC;997M = 13.15&#xD7;. EV at last close: &#x20AC;12,240M (market cap &#x20AC;10,202M + net debt &#x20AC;2,039M; PitchBook 17 Apr 2026).</p>
    </div>
    <div class="lcard">
      <div class="lt">Post-Close Capital Structure</div>
      <div class="ls">Total debt &#x20AC;5,982M at 5.0% flat rate. Debt is 46% of total transaction value. After RRD sale in Year 3, &#x20AC;2,991M (50%) is repaid from proceeds, halving the interest burden in Years 4 and 5.</div>
      <table class="s" style="margin-bottom:12px;">
        <thead><tr><th>Capital Item</th><th style="text-align:right">&#x20AC;M</th><th style="text-align:right">% of Total</th><th style="text-align:right">Rate</th></tr></thead>
        <tbody>
          <tr><td>Equity &#x2014; New co-investors</td><td style="text-align:right">2,131</td><td style="text-align:right">16%</td><td style="text-align:right">&#x2014;</td></tr>
          <tr><td>Equity &#x2014; Rossini (existing, rolled)</td><td style="text-align:right">5,002</td><td style="text-align:right">38%</td><td style="text-align:right">&#x2014;</td></tr>
          <tr><td><strong>Total Equity</strong></td><td style="text-align:right"><strong>7,133</strong></td><td style="text-align:right"><strong>54%</strong></td><td style="text-align:right">&#x2014;</td></tr>
          <tr><td>Refinanced existing debt</td><td style="text-align:right">2,467</td><td style="text-align:right">19%</td><td style="text-align:right">5.0%</td></tr>
          <tr><td>New term loan (free float buyout)</td><td style="text-align:right">3,515</td><td style="text-align:right">27%</td><td style="text-align:right">5.0%</td></tr>
          <tr><td><strong>Total Debt</strong></td><td style="text-align:right"><strong>5,982</strong></td><td style="text-align:right"><strong>46%</strong></td><td style="text-align:right">5.0%</td></tr>
          <tr class="tr"><td><strong>Total</strong></td><td style="text-align:right"><strong>13,115</strong></td><td style="text-align:right"><strong>100%</strong></td><td style="text-align:right"></td></tr>
        </tbody>
      </table>
      <table class="s">
        <thead><tr><th>Debt Metric</th><th style="text-align:right">Years 1&#x2013;3</th><th style="text-align:right">Years 4&#x2013;5</th></tr></thead>
        <tbody>
          <tr><td>Total debt outstanding</td><td style="text-align:right">&#x20AC;5,982M</td><td style="text-align:right">&#x20AC;2,991M</td></tr>
          <tr><td>Annual interest (5.0%)</td><td style="text-align:right">&#x20AC;299M</td><td style="text-align:right">&#x20AC;150M</td></tr>
          <tr><td>Y1 EBITDA / Interest coverage</td><td style="text-align:right">3.3&#xD7;</td><td style="text-align:right">&#x2014;</td></tr>
          <tr><td>Debt / Entry EBITDA at close</td><td style="text-align:right">6.0&#xD7;</td><td style="text-align:right">3.0&#xD7;</td></tr>
        </tbody>
      </table>
      <div class="dnote">50% of total group debt (&#x20AC;2,991M) is repaid from RRD sale proceeds at Year 3. The remaining &#x20AC;2,991M stays with the private entity. FCF generated across all five years (Y1 through Y5) reduces the ending debt balance before the SPC exit. Ending debt = Opening debt &#x20AC;5,982M less &#x20AC;2,991M RRD repayment less cumulative FCF Y1&#x2013;Y5.</div>
    </div>
  </div>

  <!-- MODEL NOTE -->
  <div style="background:#FBF6EC;border:1px solid var(--gold);border-radius:6px;padding:14px 17px;margin-bottom:22px;">
    <div style="font-family:'EB Garamond',serif;font-size:15px;color:var(--navy);margin-bottom:6px;">Model Assumptions and Structure</div>
    <p style="font-size:12px;color:var(--g800);line-height:1.65;">Year 1 revenue is the FY2026 management guidance midpoint of &#x20AC;2,765M. Year 1 EBITDA is &#x20AC;999M (36.1% implied margin, reflecting guided performance). From Year 2, EBITDA is modelled at a flat 35% margin applied to revenue. Revenue grows at the scenario rate for the full consolidated group in Years 1&#x2013;3. After the RRD division is sold in Year 3, Years 4 and 5 reflect SPC-only revenue (41% of Year 3 group revenue) growing at the same scenario rate. Capex is 4% of revenue throughout all five years. NWC is &#x20AC;50M per year in Years 1&#x2013;3 and &#x20AC;20.5M in Years 4&#x2013;5. Tax rate is 24% (Italy IRES). Returns are calculated on total equity invested (&#x20AC;7,133M). MOIC = ending equity / beginning equity. IRR uses timed cash flows: &#x2212;&#x20AC;7,133M at Year 0, RRD gross-to-equity at Year 3, residual SPC equity at Year 5. Ending debt = &#x20AC;5,982M less &#x20AC;2,991M RRD repayment less total FCF (Y1&#x2013;Y5). Ending equity = combined exit proceeds less ending debt. All figures are illustrative estimates and do not constitute financial projections.</p>
  </div>

  <!-- SCENARIO TABS -->
  <div class="stabs">
    <button class="stab on" onclick="showSc('base',this)">Base Case</button>
    <button class="stab" onclick="showSc('bull',this)">Bull Case</button>
    <button class="stab" onclick="showSc('bear',this)">Bear Case</button>
  </div>

  <!-- BASE CASE -->
  <div class="sp on" id="sc-base">
    <div style="background:#EAF0FA;padding:11px 15px;border-radius:5px;margin-bottom:13px;font-size:12.5px;color:var(--navy);"><strong>Base Case:</strong> Revenue grows at 6% per year across the full group. EBITDA margin 35% from Year 2. RRD sold at 15&#xD7; EBITDA in Year 3. 50% of group debt (&#x20AC;2,991M) repaid from proceeds. SPC exits at 11&#xD7; in Year 5.</div>
    <div style="overflow-x:auto;">
    <table class="cft">
      <thead><tr><th>&#x20AC; Millions</th><th>Year 1</th><th>Year 2</th><th>Year 3</th><th>Year 4</th><th>Year 5</th></tr></thead>
      <tbody>
        <tr class="sec"><td colspan="6">Income Statement</td></tr>
        <tr><td>Revenue</td><td>2,765</td><td>2,931</td><td>3,107</td><td>1,350</td><td>1,431</td></tr>
        <tr><td>EBITDA</td><td>999</td><td>1,026</td><td>1,087</td><td>473</td><td>501</td></tr>
        <tr><td>D&amp;A</td><td>(20)</td><td>(20)</td><td>(20)</td><td>(8)</td><td>(8)</td></tr>
        <tr><td>EBIT</td><td>979</td><td>1,006</td><td>1,067</td><td>465</td><td>493</td></tr>
        <tr><td>Interest expense</td><td>(299)</td><td>(299)</td><td>(299)</td><td>(150)</td><td>(150)</td></tr>
        <tr><td>EBT</td><td>680</td><td>707</td><td>768</td><td>315</td><td>343</td></tr>
        <tr><td>Tax (24%)</td><td>(163)</td><td>(170)</td><td>(184)</td><td>(76)</td><td>(82)</td></tr>
        <tr class="sub"><td>Net Income</td><td>517</td><td>537</td><td>584</td><td>240</td><td>261</td></tr>
        <tr class="sec"><td colspan="6">Free Cash Flow</td></tr>
        <tr><td>Net Income</td><td>517</td><td>537</td><td>584</td><td>240</td><td>261</td></tr>
        <tr><td>D&amp;A (add back)</td><td>20</td><td>20</td><td>20</td><td>8</td><td>8</td></tr>
        <tr><td>Capex (4% of revenue)</td><td>(111)</td><td>(117)</td><td>(124)</td><td>(54)</td><td>(57)</td></tr>
        <tr><td>Change in Net Working Capital</td><td>(50)</td><td>(50)</td><td>(50)</td><td>(21)</td><td>(21)</td></tr>
        <tr class="hl"><td>Free Cash Flow</td><td>376</td><td>390</td><td>430</td><td>172</td><td>191</td></tr>
        <tr class="hl"><td>EBITDA / Interest Coverage</td><td>3.3&#xD7;</td><td>3.4&#xD7;</td><td>3.6&#xD7;</td><td>3.2&#xD7;</td><td>3.3&#xD7;</td></tr>
        <tr class="sec"><td colspan="6">Year 3 &#x2014; RRD Division Sale at 15&#xD7;</td></tr>
        <tr><td>RRD EBITDA at sale (59% of Year 3 group EBITDA)</td><td></td><td></td><td>642</td><td></td><td></td></tr>
        <tr><td>RRD Enterprise Value (15&#xD7;)</td><td></td><td></td><td>9,623</td><td></td><td></td></tr>
        <tr><td>50% of group debt repaid from proceeds</td><td></td><td></td><td>(2,991)</td><td></td><td></td></tr>
        <tr class="gr"><td>Gross to exit equity</td><td></td><td></td><td>6,632</td><td></td><td></td></tr>
        <tr class="sec"><td colspan="6">Year 5 &#x2014; SPC Exit at 11&#xD7; (IPO or strategic sale)</td></tr>
        <tr><td>SPC EBITDA (Year 5)</td><td></td><td></td><td></td><td></td><td>501</td></tr>
        <tr><td>SPC Enterprise Value (11&#xD7;)</td><td></td><td></td><td></td><td></td><td>5,510</td></tr>
        <tr class="sec"><td colspan="6">Returns &#x2014; Total Equity Invested &#x20AC;7,133M</td></tr>
        <tr><td>Opening debt</td><td colspan="5">5,982</td></tr>
        <tr><td>Less: RRD debt repayment (Year 3)</td><td colspan="5">(2,991)</td></tr>
        <tr><td>Less: Total FCF generated (Y1&#x2013;Y5)</td><td colspan="5">(1,559)</td></tr>
        <tr><td>Ending debt</td><td colspan="5">1,432</td></tr>
        <tr><td>Combined exit proceeds (RRD &#x20AC;9,623 + SPC &#x20AC;5,510 less debt settled &#x20AC;2,991)</td><td colspan="5">12,142</td></tr>
        <tr><td>Ending equity (combined proceeds less ending debt)</td><td colspan="5">10,710</td></tr>
        <tr class="hl"><td>MOIC (&#x20AC;10,710 / &#x20AC;7,133)</td><td colspan="5">1.50&#xD7;</td></tr>
        <tr class="hl"><td>IRR (timed: &#x2212;&#x20AC;7,133 Y0 | &#x20AC;6,632 Y3 | &#x20AC;4,078 Y5)</td><td colspan="5">9.1%</td></tr>
      </tbody>
    </table>
    </div>
    <p style="font-size:10.5px;color:var(--g400);margin-top:8px;font-style:italic;">Y4&#x2013;Y5 revenue reflects SPC-only operations (41% of Y3 group revenue, growing at 6%). Ending debt = &#x20AC;5,982M opening less &#x20AC;2,991M RRD repayment less total FCF of &#x20AC;1,559M (Y1&#x2013;Y5: &#x20AC;376 + &#x20AC;390 + &#x20AC;430 + &#x20AC;172 + &#x20AC;191). IRR timed flows: &#x2212;&#x20AC;7,133M at Y0; &#x20AC;6,632M at Y3; &#x20AC;4,078M at Y5 (ending equity &#x20AC;10,710M less Y3 cash &#x20AC;6,632M).</p>
  </div>

  <!-- BULL CASE -->
  <div class="sp" id="sc-bull">
    <div style="background:#E8F2ED;padding:11px 15px;border-radius:5px;margin-bottom:13px;font-size:12.5px;color:var(--navy);"><strong>Bull Case:</strong> Revenue grows at 10% per year, driven by accelerating Isturisa US uptake. EBITDA margin 35% from Year 2. RRD sold at 18&#xD7; in Year 3. SPC exits at 12&#xD7; in Year 5.</div>
    <div style="overflow-x:auto;">
    <table class="cft">
      <thead><tr><th>&#x20AC; Millions</th><th>Year 1</th><th>Year 2</th><th>Year 3</th><th>Year 4</th><th>Year 5</th></tr></thead>
      <tbody>
        <tr class="sec"><td colspan="6">Income Statement</td></tr>
        <tr><td>Revenue</td><td>2,765</td><td>3,042</td><td>3,346</td><td>1,509</td><td>1,660</td></tr>
        <tr><td>EBITDA</td><td>999</td><td>1,065</td><td>1,171</td><td>528</td><td>581</td></tr>
        <tr><td>D&amp;A</td><td>(20)</td><td>(20)</td><td>(20)</td><td>(8)</td><td>(8)</td></tr>
        <tr><td>EBIT</td><td>979</td><td>1,045</td><td>1,151</td><td>520</td><td>573</td></tr>
        <tr><td>Interest expense</td><td>(299)</td><td>(299)</td><td>(299)</td><td>(150)</td><td>(150)</td></tr>
        <tr><td>EBT</td><td>680</td><td>745</td><td>852</td><td>370</td><td>423</td></tr>
        <tr><td>Tax (24%)</td><td>(163)</td><td>(179)</td><td>(204)</td><td>(89)</td><td>(102)</td></tr>
        <tr class="sub"><td>Net Income</td><td>517</td><td>567</td><td>647</td><td>281</td><td>322</td></tr>
        <tr class="sec"><td colspan="6">Free Cash Flow</td></tr>
        <tr><td>Net Income</td><td>517</td><td>567</td><td>647</td><td>281</td><td>322</td></tr>
        <tr><td>D&amp;A (add back)</td><td>20</td><td>20</td><td>20</td><td>8</td><td>8</td></tr>
        <tr><td>Capex (4% of revenue)</td><td>(111)</td><td>(122)</td><td>(134)</td><td>(60)</td><td>(66)</td></tr>
        <tr><td>Change in Net Working Capital</td><td>(50)</td><td>(50)</td><td>(50)</td><td>(21)</td><td>(21)</td></tr>
        <tr class="hl"><td>Free Cash Flow</td><td>376</td><td>415</td><td>483</td><td>208</td><td>243</td></tr>
        <tr class="hl"><td>EBITDA / Interest Coverage</td><td>3.3&#xD7;</td><td>3.6&#xD7;</td><td>3.9&#xD7;</td><td>3.5&#xD7;</td><td>3.9&#xD7;</td></tr>
        <tr class="sec"><td colspan="6">Year 3 &#x2014; RRD Division Sale at 18&#xD7;</td></tr>
        <tr><td>RRD EBITDA at sale (59% of Year 3 group EBITDA)</td><td></td><td></td><td>691</td><td></td><td></td></tr>
        <tr><td>RRD Enterprise Value (18&#xD7;)</td><td></td><td></td><td>12,436</td><td></td><td></td></tr>
        <tr><td>50% of group debt repaid from proceeds</td><td></td><td></td><td>(2,991)</td><td></td><td></td></tr>
        <tr class="gr"><td>Gross to exit equity</td><td></td><td></td><td>9,445</td><td></td><td></td></tr>
        <tr class="sec"><td colspan="6">Year 5 &#x2014; SPC Exit at 12&#xD7;</td></tr>
        <tr><td>SPC EBITDA (Year 5)</td><td></td><td></td><td></td><td></td><td>581</td></tr>
        <tr><td>SPC Enterprise Value (12&#xD7;)</td><td></td><td></td><td></td><td></td><td>6,971</td></tr>
        <tr class="sec"><td colspan="6">Returns &#x2014; Total Equity Invested &#x20AC;7,133M</td></tr>
        <tr><td>Opening debt</td><td colspan="5">5,982</td></tr>
        <tr><td>Less: RRD debt repayment (Year 3)</td><td colspan="5">(2,991)</td></tr>
        <tr><td>Less: Total FCF generated (Y1&#x2013;Y5)</td><td colspan="5">(1,725)</td></tr>
        <tr><td>Ending debt</td><td colspan="5">1,266</td></tr>
        <tr><td>Combined exit proceeds (RRD &#x20AC;12,436 + SPC &#x20AC;6,971 less debt settled &#x20AC;2,991)</td><td colspan="5">16,416</td></tr>
        <tr><td>Ending equity (combined proceeds less ending debt)</td><td colspan="5">15,150</td></tr>
        <tr class="hl"><td>MOIC (&#x20AC;15,150 / &#x20AC;7,133)</td><td colspan="5">2.12&#xD7;</td></tr>
        <tr class="hl"><td>IRR (timed: &#x2212;&#x20AC;7,133 Y0 | &#x20AC;9,445 Y3 | &#x20AC;5,705 Y5)</td><td colspan="5">16.4%</td></tr>
      </tbody>
    </table>
    </div>
    <p style="font-size:10.5px;color:var(--g400);margin-top:8px;font-style:italic;">Ending debt = &#x20AC;5,982M less &#x20AC;2,991M less total FCF of &#x20AC;1,725M (Y1&#x2013;Y5: &#x20AC;376 + &#x20AC;415 + &#x20AC;483 + &#x20AC;208 + &#x20AC;243). IRR timed flows: &#x2212;&#x20AC;7,133M at Y0; &#x20AC;9,445M at Y3; &#x20AC;5,705M at Y5 (ending equity &#x20AC;15,150M less Y3 cash &#x20AC;9,445M).</p>
  </div>

  <!-- BEAR CASE -->
  <div class="sp" id="sc-bear">
    <div style="background:var(--redl);padding:11px 15px;border-radius:5px;margin-bottom:13px;font-size:12.5px;color:#7A1010;border-left:3px solid #C0392B;"><strong>Bear Case:</strong> Revenue grows at 3% per year, reflecting FX headwinds, slower Isturisa uptake and Cardicor licence loss drag. EBITDA margin 35% from Year 2. RRD sold at 12&#xD7; with no strategic premium. SPC exits at 9&#xD7;.</div>
    <div style="overflow-x:auto;">
    <table class="cft">
      <thead><tr><th>&#x20AC; Millions</th><th>Year 1</th><th>Year 2</th><th>Year 3</th><th>Year 4</th><th>Year 5</th></tr></thead>
      <tbody>
        <tr class="sec"><td colspan="6">Income Statement</td></tr>
        <tr><td>Revenue</td><td>2,765</td><td>2,848</td><td>2,933</td><td>1,239</td><td>1,276</td></tr>
        <tr><td>EBITDA</td><td>999</td><td>997</td><td>1,027</td><td>434</td><td>447</td></tr>
        <tr><td>D&amp;A</td><td>(20)</td><td>(20)</td><td>(20)</td><td>(8)</td><td>(8)</td></tr>
        <tr><td>EBIT</td><td>979</td><td>977</td><td>1,007</td><td>425</td><td>438</td></tr>
        <tr><td>Interest expense</td><td>(299)</td><td>(299)</td><td>(299)</td><td>(150)</td><td>(150)</td></tr>
        <tr><td>EBT</td><td>680</td><td>678</td><td>708</td><td>276</td><td>289</td></tr>
        <tr><td>Tax (24%)</td><td>(163)</td><td>(163)</td><td>(170)</td><td>(66)</td><td>(69)</td></tr>
        <tr class="sub"><td>Net Income</td><td>517</td><td>515</td><td>538</td><td>210</td><td>220</td></tr>
        <tr class="sec"><td colspan="6">Free Cash Flow</td></tr>
        <tr><td>Net Income</td><td>517</td><td>515</td><td>538</td><td>210</td><td>220</td></tr>
        <tr><td>D&amp;A (add back)</td><td>20</td><td>20</td><td>20</td><td>8</td><td>8</td></tr>
        <tr><td>Capex (4% of revenue)</td><td>(111)</td><td>(114)</td><td>(117)</td><td>(50)</td><td>(51)</td></tr>
        <tr><td>Change in Net Working Capital</td><td>(50)</td><td>(50)</td><td>(50)</td><td>(21)</td><td>(21)</td></tr>
        <tr class="hl"><td>Free Cash Flow</td><td>376</td><td>371</td><td>391</td><td>148</td><td>156</td></tr>
        <tr class="hl"><td>EBITDA / Interest Coverage</td><td>3.3&#xD7;</td><td>3.3&#xD7;</td><td>3.4&#xD7;</td><td>2.9&#xD7;</td><td>3.0&#xD7;</td></tr>
        <tr class="sec"><td colspan="6">Year 3 &#x2014; RRD Division Sale at 12&#xD7;</td></tr>
        <tr><td>RRD EBITDA at sale (59% of Year 3 group EBITDA)</td><td></td><td></td><td>606</td><td></td><td></td></tr>
        <tr><td>RRD Enterprise Value (12&#xD7;)</td><td></td><td></td><td>7,269</td><td></td><td></td></tr>
        <tr><td>50% of group debt repaid from proceeds</td><td></td><td></td><td>(2,991)</td><td></td><td></td></tr>
        <tr class="gr"><td>Gross to exit equity</td><td></td><td></td><td>4,278</td><td></td><td></td></tr>
        <tr class="sec"><td colspan="6">Year 5 &#x2014; SPC Exit at 9&#xD7;</td></tr>
        <tr><td>SPC EBITDA (Year 5)</td><td></td><td></td><td></td><td></td><td>447</td></tr>
        <tr><td>SPC Enterprise Value (9&#xD7;)</td><td></td><td></td><td></td><td></td><td>4,019</td></tr>
        <tr class="sec"><td colspan="6">Returns &#x2014; Total Equity Invested &#x20AC;7,133M</td></tr>
        <tr><td>Opening debt</td><td colspan="5">5,982</td></tr>
        <tr><td>Less: RRD debt repayment (Year 3)</td><td colspan="5">(2,991)</td></tr>
        <tr><td>Less: Total FCF generated (Y1&#x2013;Y5)</td><td colspan="5">(1,442)</td></tr>
        <tr><td>Ending debt</td><td colspan="5">1,549</td></tr>
        <tr><td>Combined exit proceeds (RRD &#x20AC;7,269 + SPC &#x20AC;4,019 less debt settled &#x20AC;2,991)</td><td colspan="5">8,297</td></tr>
        <tr><td>Ending equity (combined proceeds less ending debt)</td><td colspan="5">6,748</td></tr>
        <tr class="hl"><td>MOIC (&#x20AC;6,748 / &#x20AC;7,133)</td><td colspan="5">0.95&#xD7;</td></tr>
        <tr class="hl"><td>IRR (timed: &#x2212;&#x20AC;7,133 Y0 | &#x20AC;4,278 Y3 | &#x20AC;2,470 Y5)</td><td colspan="5">(1.3)%</td></tr>
      </tbody>
    </table>
    </div>
    <div style="margin-top:13px;background:var(--redl);padding:13px 15px;border-radius:5px;border-left:3px solid #C0392B;">
      <div style="font-size:12px;font-weight:600;color:#7A1010;margin-bottom:5px;">Reading the Bear Case</div>
      <p style="font-size:12px;color:#5A1010;line-height:1.65;">In the downside scenario, co-investors lose approximately &#x20AC;385M on a &#x20AC;7,133M commitment, returning 0.95&#xD7; MOIC and a negative IRR of (1.3)%. This represents 3% revenue growth across the group, an RRD exit at 12&#xD7; with no strategic premium, and a macro-compressed SPC exit at 9&#xD7;. Interest coverage stays at 2.9&#xD7; at its lowest point, well above typical covenant floors. The loss is driven entirely by multiple compression at exit, not financial distress. Ending debt = &#x20AC;5,982M less &#x20AC;2,991M RRD repayment less cumulative FCF of &#x20AC;1,442M (Y1&#x2013;Y5: &#x20AC;376 + &#x20AC;371 + &#x20AC;391 + &#x20AC;148 + &#x20AC;156).</p>
    </div>
  </div>

  <!-- ICR Summary -->
  <div class="mt24">
    <h3 style="font-family:'EB Garamond',serif;font-size:17px;color:var(--navy);margin-bottom:11px;">EBITDA Interest Coverage &#x2014; All Scenarios, All Years</h3>
    <div class="icrg">
      <div class="icrc ok"><div class="icrv">3.9&#xD7;</div><div class="icrl">Bull &#x2014; Year 3 and Year 5 peak</div></div>
      <div class="icrc ok"><div class="icrv">3.3&#xD7;</div><div class="icrl">Base &#x2014; Year 1 (&#x20AC;999M / &#x20AC;299M)</div></div>
      <div class="icrc ok"><div class="icrv">3.3&#xD7;</div><div class="icrl">Bear &#x2014; Year 1 minimum</div></div>
      <div class="icrc ok"><div class="icrv">2.9&#xD7;</div><div class="icrl">Bear &#x2014; Year 4 (post-RRD, lowest point)</div></div>
      <div class="icrc ok"><div class="icrv">1.5&#xD7;</div><div class="icrl">Typical lender covenant floor</div></div>
    </div>
    <p style="font-size:11px;color:var(--g400);margin-top:9px;font-style:italic;">Debt of &#x20AC;5,982M at 5.0% generates &#x20AC;299.1M of annual interest in Years 1&#x2013;3. Post-RRD, &#x20AC;2,991M is repaid and interest falls to &#x20AC;149.6M. Even in the bear case, EBITDA covers interest at 2.9&#xD7; at its lowest point (Year 4). All scenarios remain well above typical covenant floors throughout the hold period. Total transaction value: &#x20AC;13,115M. Equity: &#x20AC;7,133M (54%). Debt: &#x20AC;5,982M (46%). Entry EV/EBITDA: 13.15&#xD7;. Returns on total equity (&#x20AC;7,133M). All figures are illustrative estimates.</p>
  </div>
</div>
</div>


<!-- CAP TABLE ══════════════════════════════════════════════════ -->
<div class="panel" id="p-captable">
<div class="pi">
  <div class="ey">Capital Structure</div>
  <h2 class="st">Current Ownership — Pre Transaction</h2>
  <div class="dv"></div>
  <p class="ss">As of 17 April 2026. CVC holds 46.8% through Rossini HoldCo alongside PSP, StepStone and AlpInvest. The cash offer targets the 53.2% free float only. Existing consortium partners roll their stakes into the new private structure.</p>
  <div class="capw">
    <div>
      <div class="capch"><canvas id="capChart"></canvas></div>
      <div class="capleg" id="capLeg"></div>
    </div>
    <div>
      <h3 style="font-size:16px;color:var(--navy);margin-bottom:15px;">Shareholder Detail</h3>
      <table class="s">
        <thead><tr><th>Shareholder</th><th>Stake</th><th>Vehicle</th><th>Type</th></tr></thead>
        <tbody>
          <tr><td><strong>CVC Capital Partners</strong><br><span style="font-size:11px;color:var(--g400);">Lead sponsor</span></td><td><strong>31.5%</strong></td><td style="font-size:11px;color:var(--g600);">Rossini HoldCo (Luxembourg)</td><td><span class="bx bl">Lead</span></td></tr>
          <tr><td><strong>PSP Investments</strong><br><span style="font-size:11px;color:var(--g400);">Canadian PPF · C$264bn</span></td><td><strong>6.0%</strong></td><td style="font-size:11px;color:var(--g600);">Via Rossini HoldCo</td><td><span class="bx bc">Existing Co-investor</span></td></tr>
          <tr><td><strong>StepStone Group</strong><br><span style="font-size:11px;color:var(--g400);">PE co-investment · $700bn</span></td><td><strong>5.5%</strong></td><td style="font-size:11px;color:var(--g600);">Via Rossini HoldCo</td><td><span class="bx bc">Existing Co-investor</span></td></tr>
          <tr><td><strong>AlpInvest Partners</strong><br><span style="font-size:11px;color:var(--g400);">Carlyle subsidiary · ~$100bn</span></td><td><strong>3.8%</strong></td><td style="font-size:11px;color:var(--g600);">Via Rossini HoldCo</td><td><span class="bx bc">Existing Co-investor</span></td></tr>
          <tr><td><strong>Free Float</strong><br><span style="font-size:11px;color:var(--g400);">Borsa Italiana (MIL: REC)</span></td><td><strong>53.2%</strong></td><td style="font-size:11px;color:var(--g600);">Public market</td><td><span class="bx bf">Cash Tender Target</span></td></tr>
          <tr class="tr"><td><strong>Total</strong></td><td><strong>100%</strong></td><td></td><td></td></tr>
        </tbody>
      </table>
      <div class="capn mt16">
        <div class="capnt">The Co-Investment Structure</div>
        <div class="capnd">Incoming co-investors participate in the cash tender offer alongside CVC. Their capital goes directly to acquire free float shares at €52 per share — a 4.0% premium to the last close of €50.00 on 17 April 2026. There is no fund layer, no management fee and no carried interest. The new entity post-close will be owned by CVC, Rossini rolling partners and incoming co-investors in proportion to their capital contributions.</div>
      </div>
    </div>
  </div>
</div>
</div>

<!-- DEAL STRUCTURE ══════════════════════════════════════════════ -->
<div class="panel" id="p-deal">
<div class="pi">
  <div class="ey">Transaction</div>
  <h2 class="st">How the Deal Works</h2>
  <div class="dv"></div>
  <div class="dgrid">
    <div>
      <div class="dsumm">
        <div class="dst">Transaction Summary</div>
        <div class="dsr"><span class="dsl">Offer price</span><span class="dsv g">€52.00 per share</span></div>
        <div class="dsr"><span class="dsl">Last close (17 April 2026)</span><span class="dsv">€50.00</span></div>
        <div class="dsr"><span class="dsl">Premium to last close</span><span class="dsv">4.0%</span></div>
        <div class="dsr"><span class="dsl">Equity value (market cap)</span><span class="dsv g">€10.11bn</span></div>
        <div class="dsr"><span class="dsl">Net debt (PitchBook, 17 Apr 2026)</span><span class="dsv">€2.039bn</span></div>
        <div class="dsr"><span class="dsl">Enterprise value (PitchBook, 17 Apr 2026)</span><span class="dsv g">€12.24bn</span></div>
        <div class="dsr"><span class="dsl">Entry EV / FY2025 EBITDA</span><span class="dsv">12.35&#xD7;</span></div>
        <div class="dsr"><span class="dsl">Forward EV / FY2026 EBITDA</span><span class="dsv">12.18&#xD7; (PitchBook)</span></div>
        <div class="dsr"><span class="dsl">Cash required for free float</span><span class="dsv">€5,641M</span></div>
        <div class="dsr"><span class="dsl">New co-investor equity</span><span class="dsv">&#x20AC;2,131M (free float + 30% of fees)</span></div>
        <div class="dsr"><span class="dsl">Total debt in private entity</span><span class="dsv">&#x20AC;5,982M (46% of deal · 5.0%)</span></div>
        <div class="dsr"><span class="dsl">Expected close</span><span class="dsv">H2 2026</span></div>
        <div class="dsr"><span class="dsl">Base case IRR (total equity)</span><span class="dsv gr">9.1% (timed cash flows)</span></div>
      </div>
      <div class="steps mt20">
        <div class="step"><div class="sn">1</div><div><h4>Cash tender offer to free float shareholders</h4><p>A consortium of new co-investors (&#x20AC;2,131M) and the Rossini consortium (rolling &#x20AC;5,002M) acquires 100% of Recordati. &#x20AC;3,515M of new debt funds the free float purchase alongside existing debt of &#x20AC;2,467M refinanced. Total transaction value: &#x20AC;13,115M.</p></div></div>
        <div class="step"><div class="sn">2</div><div><h4>Delisting and private restructuring</h4><p>Following completion of the tender offer, Recordati is delisted from Borsa Italiana. The PE ownership overhang, Italian listing discount and conglomerate blending problem are all resolved simultaneously. The rare disease division is operationally separated from specialty pharma.</p></div></div>
        <div class="step"><div class="sn">3</div><div><h4>Rare disease division sale in Year 2 to Year 3</h4><p>The rare disease division — growing at 30% annually, anchored by Isturisa and Enjaymo — is sold to a pharmaceutical strategic buyer or listed separately at 18 to 22× EBITDA. Proceeds of approximately €12bn to €14bn at base case fully repay acquisition debt and return capital to equity holders.</p></div></div>
      </div>
    </div>
    <div>
      <div style="font-size:11px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;color:var(--g600);margin-bottom:9px;">Sum-of-the-parts value bridge</div>
      <div class="cc">
        <div class="ct">SOTP Valuation vs Entry EV</div>
        <div class="cs">Entry EV €12.24bn vs estimated SOTP range &#x20AC;12.2 to &#x20AC;15.0bn · &#x20AC;bn</div>
        <div class="cw" style="height:220px;"><canvas id="sotpChart"></canvas></div>
      </div>
      <div class="mt20">
        <table class="s">
          <thead><tr><th>Division</th><th>Revenue</th><th>Est. EBITDA</th><th>Multiple</th><th>Value</th></tr></thead>
          <tbody>
            <tr><td><strong>Rare Disease (RRD)</strong></td><td>€1,081M</td><td>€435M</td><td>18 to 22×</td><td><strong>€7.8 to 9.6bn</strong></td></tr>
            <tr><td><strong>Specialty Pharma (SPC)</strong></td><td>€1,478M</td><td>€490M</td><td>9 to 11×</td><td><strong>€4.4 to 5.4bn</strong></td></tr>
            <tr class="tr"><td><strong>SOTP Total</strong></td><td></td><td>€925M</td><td></td><td><strong>€12.2 to 15.0bn</strong></td></tr>
          </tbody>
        </table>
        <p style="font-size:10.5px;color:var(--g400);margin-top:9px;font-style:italic;">EBITDA allocations are illustrative estimates based on an assumed RRD margin of 38 to 40% versus the blended group margin of 37.8%. These figures are indicative and do not constitute financial projections.</p>
      </div>
    </div>
  </div>
</div>
</div>

<!-- MARKET ══════════════════════════════════════════════════════ -->
<div class="panel" id="p-market">
<div class="pi">
  <div class="ey">Rare Disease Market</div>
  <h2 class="st">A Structural Growth Market With High Barriers</h2>
  <div class="dv"></div>
  <div class="mkpi">
    <div class="mk"><div class="mkl">Global Rare Disease Market 2024</div><div class="mkv">$154.6bn</div><div class="mkn">Projected $495bn by 2033</div></div>
    <div class="mk"><div class="mkl">Market CAGR 2024 to 2033</div><div class="mkv">13.8%</div><div class="mkn">DataM Intelligence 2024</div></div>
    <div class="mk"><div class="mkl">Recordati Rare Disease Revenue YoY</div><div class="mkv">+29.7%</div><div class="mkn">FY2025 vs FY2024</div></div>
    <div class="mk"><div class="mkl">Average Diagnosis Delay</div><div class="mkv">4 to 5 years</div><div class="mkn">Persistent structural demand</div></div>
  </div>
  <div class="cgrid">
    <div class="cc">
      <div class="ct">Global Rare Disease Market Growth</div>
      <div class="cs">2023 to 2033E · $bn · CAGR of 13.8% · DataM Intelligence 2024</div>
      <div class="cw"><canvas id="marketChart"></canvas></div>
    </div>
    <div>
      <div style="font-size:11px;font-weight:500;letter-spacing:.07em;text-transform:uppercase;color:var(--g600);margin-bottom:9px;">11 Marketed Rare Disease Drugs — Full Portfolio</div>
      <div class="dtcard">
        <div class="dthdr">
          <span>Drug (Brand Name)</span>
          <span>Indication</span>
          <span style="text-align:center;">Area</span>
        </div>
        <div class="dtrow"><div>Isturisa® (osilodrostat)</div><div>Cushing's Syndrome</div><div><span class="bx bm">Endocrinology</span></div></div>
        <div class="dtrow"><div>Signifor® (pasireotide)</div><div>Cushing's Disease / Acromegaly</div><div><span class="bx bm">Endocrinology</span></div></div>
        <div class="dtrow"><div>Signifor® LAR (pasireotide)</div><div>Acromegaly</div><div><span class="bx bm">Endocrinology</span></div></div>
        <div class="dtrow"><div>Enjaymo® (sutimlimab)</div><div>Cold Agglutinin Disease</div><div><span class="bx" style="background:#EEF0FE;color:#3C3489;">Haematology</span></div></div>
        <div class="dtrow"><div>Sylvant® (siltuximab)</div><div>Castleman Disease (iMCD)</div><div><span class="bx bp">Oncology</span></div></div>
        <div class="dtrow"><div>Qarziba® (dinutuximab beta)</div><div>High-Risk Neuroblastoma</div><div><span class="bx bp">Oncology</span></div></div>
        <div class="dtrow"><div>Panhematin® (hemin)</div><div>Acute Porphyria (US)</div><div><span class="bx" style="background:#F1EFE8;color:#444441;">Metabolism</span></div></div>
        <div class="dtrow"><div>Normosang® (heme arginate)</div><div>Acute Porphyria (Europe)</div><div><span class="bx" style="background:#F1EFE8;color:#444441;">Metabolism</span></div></div>
        <div class="dtrow"><div>Carbaglu® (carglumic acid)</div><div>NAGS Deficiency / Organic Acidemia</div><div><span class="bx" style="background:#F1EFE8;color:#444441;">Metabolism</span></div></div>
        <div class="dtrow"><div>Cystadane® (betaine anhydrous)</div><div>Homocystinuria</div><div><span class="bx" style="background:#F1EFE8;color:#444441;">Metabolism</span></div></div>
        <div class="dtrow"><div>Cystadrops® (cysteamine)</div><div>Cystinosis</div><div><span class="bx" style="background:#F1EFE8;color:#444441;">Metabolism</span></div></div>
      </div>
    </div>
  </div>
</div>
</div>

<!-- CO-INVESTORS ════════════════════════════════════════════════ -->
<div class="panel" id="p-coinvestors">
<div class="pi">
  <div class="ey">Co-Investor Universe</div>
  <h2 class="st">Who CVC Is Approaching</h2>
  <div class="dv"></div>
  <p class="ss">Selected investors across private equity firms, sovereign wealth funds, pension funds and strategic holding companies.</p>
  <div class="ittl">Tier 1 — Rossini HoldCo Partners Rolling Into the New Structure</div>
  <div class="ir" style="font-size:10.5px;color:var(--g400);font-weight:500;padding:4px 0;border-bottom:2px solid var(--g200);"><span>Investor</span><span>AUM</span><span>Rationale</span><span>Status</span></div>
  <div class="ir"><div><div class="in">PSP Investments</div><div class="it">Canadian Public Pension</div></div><div class="ia">C$264bn</div><div class="ino">Original 2018 consortium member with zero incremental diligence required. PSP rolls its existing stake rather than deploying new capital, simplifying the close process.</div><div><span class="fp fs">Priority</span></div></div>
  <div class="ir"><div><div class="in">StepStone Group</div><div class="it">PE Co-Investment Platform</div></div><div class="ia">$700bn</div><div class="ino">Co-investment specialist that was part of the original 2018 deal. Established relationship with CVC management and deep familiarity with the asset.</div><div><span class="fp fs">Priority</span></div></div>
  <div class="ir"><div><div class="in">AlpInvest Partners</div><div class="it">Carlyle Subsidiary</div></div><div class="ia">~$100bn</div><div class="ino">Secondary and co-investment mandate. Rolling Rossini stake. CVC approaches first given existing relationship.</div><div><span class="fp fs">Priority</span></div></div>
  <div class="ittl">Tier 2 — Confirmed in Active Discussions with CVC (Bloomberg, April 2026)</div>
  <div class="ir"><div><div class="in">ADIA</div><div class="it">Abu Dhabi Sovereign Wealth Fund</div></div><div class="ia">~$1.1tn</div><div class="ino">Co-invested 26% in the Dechra pharma take-private in 2023. Co-invested in Hologic alongside Blackstone and TPG in 2025. Healthcare public-to-private transactions are a core programme for ADIA.</div><div><span class="fp fs">In Talks</span></div></div>
  <div class="ir"><div><div class="in">GIC</div><div class="it">Singapore Sovereign Wealth Fund</div></div><div class="ia">~$800bn</div><div class="ino">Invested in Cimed pharma in 2025 and co-invested in Hologic alongside ADIA in the same year. GIC operates on a twenty year horizon, making a five-year hold structure well-suited to its mandate.</div><div><span class="fp fs">In Talks</span></div></div>
  <div class="ir"><div><div class="in">CDPQ</div><div class="it">Quebec Pension Fund</div></div><div class="ia">C$517bn</div><div class="ino">Private equity returned 17.2% in 2024. The Paris office is active in large European transactions and the fund targets C$20bn in private equity deployment annually.</div><div><span class="fp fs">In Talks</span></div></div>
  <div class="ir"><div><div class="in">GBL</div><div class="it">Belgian Strategic Holding Company</div></div><div class="ia">NAV €14bn</div><div class="ino">Healthcare platforms drove €584M of NAV growth in 2025. Loan-to-value at zero gives GBL full balance sheet capacity and the company is reinvesting €3bn into private assets by 2027.</div><div><span class="fp fs">In Talks</span></div></div>

</div>
</div>

<!-- RETURNS ════════════════════════════════════════════════════ -->
<div class="panel" id="p-returns">
<div class="pi">
  <div class="ey">Returns Analysis</div>
  <h2 class="st">What Investors Stand to Make</h2>
  <div class="dv"></div>
  <p class="ss">All figures are illustrative only. Returns are calculated on total equity invested (&#x20AC;7,133M), comprising new co-investor equity of &#x20AC;2,131M and the Rossini rollover of &#x20AC;5,002M. Cash flows: &#x2212;&#x20AC;7,133M at Year 0, RRD gross-to-equity received at Year 3, and residual SPC equity at Year 5. Debt of &#x20AC;5,982M at 5.0% generates &#x20AC;299M of annual interest, covered 3.3&#xD7; by Year 1 EBITDA. The returns are driven principally by RRD exit multiple expansion from the 13.15&#xD7; entry to 15&#x2013;18&#xD7; at sale, amplified by financial leverage.</p>
  <div class="rgrid">
    <div class="sc bear">
      <div class="sch"><h3>Bear Case</h3><span class="sct">True Downside — No Growth</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">Scenario summary</span><span class="ssv">Flat revenue, no multiple expansion</span></div>
        <div class="ss2"><span class="ssl">RRD exit multiple</span><span class="ssv">12× (entry multiple)</span></div>
        <div class="ss2"><span class="ssl">SPC exit multiple</span><span class="ssv">9×</span></div>
        <div class="ss2"><span class="ssl">Hold period</span><span class="ssv">5 years</span></div>
        <div class="ss2"><span class="ssl">RRD exit multiple</span><span class="ssv">12&#xD7; (no expansion)</span></div>
        <div class="ss2"><span class="ssl">SPC exit multiple</span><span class="ssv">9&#xD7;</span></div>
        <div class="ss2"><span class="ssl">Co-investor cash out (Year 5)</span><span class="ssv">&#x20AC;4.0bn</span></div>
        <div class="ss2"><span class="ssl">Total equity invested</span><span class="ssv">&#x20AC;7,133M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi" style="color:#C0392B;">0.95&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv" style="color:#C0392B;">(1.3)%</span></div>
      </div>
    </div>
    <div class="sc base">
      <div class="sch"><h3>Base Case</h3><span class="sct">RRD at 18× · Year 3 Sale</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">Scenario summary</span><span class="ssv">6% CAGR, RRD carve-out Year 3</span></div>
        <div class="ss2"><span class="ssl">RRD exit multiple</span><span class="ssv">18× EBITDA</span></div>
        <div class="ss2"><span class="ssl">RRD proceeds to equity</span><span class="ssv">€7.4bn</span></div>
        <div class="ss2"><span class="ssl">SPC exit at Year 5 (10×)</span><span class="ssv">€5.0bn</span></div>
        <div class="ss2"><span class="ssl">RRD gross to equity (Year 3, 15&#xD7;)</span><span class="ssv">&#x20AC;6,632M</span></div>
        <div class="ss2"><span class="ssl">SPC exit EV (Year 5, 11&#xD7;)</span><span class="ssv">&#x20AC;5,510M</span></div>
        <div class="ss2"><span class="ssl">Ending equity</span><span class="ssv">&#x20AC;10,710M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi">1.50&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv">9.1%</span></div>
      </div>
    </div>
    <div class="sc bull">
      <div class="sch"><h3>Bull Case</h3><span class="sct">RRD at 22× · Year 2 Sale</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">Scenario summary</span><span class="ssv">9% CAGR, RRD carve-out Year 2</span></div>
        <div class="ss2"><span class="ssl">RRD exit multiple</span><span class="ssv">22× EBITDA</span></div>
        <div class="ss2"><span class="ssl">RRD proceeds to equity</span><span class="ssv">€9.5bn</span></div>
        <div class="ss2"><span class="ssl">SPC exit at Year 3 (11×)</span><span class="ssv">€5.5bn</span></div>
        <div class="ss2"><span class="ssl">RRD gross to equity (Year 3, 18&#xD7;)</span><span class="ssv">&#x20AC;9,445M</span></div>
        <div class="ss2"><span class="ssl">SPC exit EV (Year 5, 12&#xD7;)</span><span class="ssv">&#x20AC;6,971M</span></div>
        <div class="ss2"><span class="ssl">Ending equity</span><span class="ssv">&#x20AC;15,150M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi">2.12&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv" style="color:var(--green);font-weight:600;">16.4%</span></div>
      </div>
    </div>
  </div>
  <div class="cc mt20">
    <div class="ct">IRR Sensitivity — Exit Multiple vs Hold Period</div>
    <div class="cs">Illustrative returns &#xB7; Total equity &#x20AC;7,133M &#xB7; Debt &#x20AC;5,982M at 5.0% &#xB7; Base 1.50&#xD7; MOIC / 9.1% IRR &#xB7; RRD sold Year 3, SPC exits Year 5</div>
    <div class="cw" style="height:240px;"><canvas id="irrChart"></canvas></div>
    <div class="leg mt16">
      <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#243F78;"></span>Year 2 Sale</span>
      <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#0D1B3E;"></span>Year 3 Sale</span>
      <span style="display:flex;align-items:center;gap:5px;"><span class="ld" style="background:#B8964E;"></span>Year 5 Sale</span>
    </div>
  </div>
  <p style="font-size:11px;color:var(--g400);margin-top:11px;font-style:italic;">All return scenarios are illustrative only. They do not account for taxes or legal costs beyond the transaction fees in the model. Debt of &#x20AC;5,982M (6.0&#xD7; entry EBITDA) at 5.0% generates &#x20AC;299M of annual interest. The RRD exit multiple is the primary driver of returns; leverage amplifies the effect. The bear case produces a small capital loss (0.95&#xD7; MOIC) when the RRD division exits at 12&#xD7; with 3% revenue growth and the SPC exits at 9&#xD7;.</p>
</div>
</div>

<!-- SPC EXIT / EXIT STRATEGY ════════════════════════════════════════ -->
<div class="panel" id="p-ipo">
<div class="pi">
  <div class="ey">Exit Strategy</div>
  <h2 class="st">Three Paths to Monetisation — and What Remains After the RRD Sale</h2>
  <div class="dv"></div>
  <p class="ss">When the rare disease division is sold in Year 3, all Isturisa, Enjaymo and Signifor revenue leaves the consolidated group. What remains is the Specialty and Primary Care business — a profitable, cash-generative European branded pharma platform with four distinct franchises and a pipeline of pending approvals. The SPC business can be sold as a single block to a strategic acquirer seeking European specialty pharma distribution, or sold in parts with each franchise going to the most natural buyer. Geographic expansion into new markets, particularly across Central and Eastern Europe and the Middle East, provides an additional lever to grow revenue and improve exit pricing before the Year 5 sale.</p>

  <!-- WHAT SPC IS -->
  <div style="background:var(--navy);border-radius:8px;padding:22px 24px;margin-bottom:24px;">
    <div style="font-family:'EB Garamond',serif;font-size:18px;color:var(--gold);margin-bottom:14px;">What the Residual SPC Business Actually Contains</div>
    <p style="font-size:12.5px;color:rgba(255,255,255,.7);line-height:1.7;margin-bottom:14px;">Recordati&#x2019;s Specialty and Primary Care division generated &#x20AC;1,478M of revenue in FY2025 across four therapeutic franchises, with direct commercial operations in more than 30 countries and production facilities in Italy, France, Turkey, Spain, Czech Republic and Tunisia. After the RRD carve-out, it becomes a standalone European branded pharma business with approximately &#x20AC;540M EBITDA at Year 5 &#x2014; roughly the size of Zentiva at the time of its 2018 acquisition and comparable to STADA&#x2019;s specialty pharmaceuticals segment.</p>
    <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(255,255,255,.1);border-radius:5px;overflow:hidden;">
      <div style="background:rgba(13,27,62,.7);padding:14px 13px;">
        <div style="font-size:9.5px;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.4);margin-bottom:6px;">Urology</div>
        <div style="font-family:'EB Garamond',serif;font-size:17px;color:var(--white);">&#x20AC;490M</div>
        <div style="font-size:10.5px;color:var(--gold);margin-top:3px;">Year 5 revenue</div>
        <div style="font-size:10.5px;color:rgba(255,255,255,.5);margin-top:4px;">Eligard, Urorec, Avodart</div>
      </div>
      <div style="background:rgba(13,27,62,.7);padding:14px 13px;">
        <div style="font-size:9.5px;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.4);margin-bottom:6px;">Cardiovascular</div>
        <div style="font-family:'EB Garamond',serif;font-size:17px;color:var(--white);">&#x20AC;490M</div>
        <div style="font-size:10.5px;color:var(--gold);margin-top:3px;">Year 5 revenue</div>
        <div style="font-size:10.5px;color:rgba(255,255,255,.5);margin-top:4px;">Zanidip, Livazo, Vazkepa</div>
      </div>
      <div style="background:rgba(13,27,62,.7);padding:14px 13px;">
        <div style="font-size:9.5px;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.4);margin-bottom:6px;">Gastrointestinal</div>
        <div style="font-family:'EB Garamond',serif;font-size:17px;color:var(--white);">&#x20AC;245M</div>
        <div style="font-size:10.5px;color:var(--gold);margin-top:3px;">Year 5 revenue</div>
        <div style="font-size:10.5px;color:rgba(255,255,255,.5);margin-top:4px;">Rx and OTC portfolio</div>
      </div>
      <div style="background:rgba(13,27,62,.7);padding:14px 13px;">
        <div style="font-size:9.5px;letter-spacing:.07em;text-transform:uppercase;color:rgba(255,255,255,.4);margin-bottom:6px;">Cough &amp; Cold / OTC</div>
        <div style="font-family:'EB Garamond',serif;font-size:17px;color:var(--white);">&#x20AC;245M</div>
        <div style="font-size:10.5px;color:var(--gold);margin-top:3px;">Year 5 revenue</div>
        <div style="font-size:10.5px;color:rgba(255,255,255,.5);margin-top:4px;">Russia/CIS/Turkey focus</div>
      </div>
    </div>
  </div>

  <!-- SPC COMPARABLE TABLE -->
  <div class="cc" style="margin-bottom:24px;">
    <div class="ct">SPC Comparable Transactions — European Branded and Specialty Pharma</div>
    <div class="cs">Source: InterCapital September 2025 · PitchBook · Public filings · All multiples EV/EBITDA</div>
    <table class="s">
      <thead><tr><th>Company</th><th>Revenue</th><th>EBITDA</th><th>EV/EBITDA</th><th>Acquirer / Status</th><th>What makes it comparable</th></tr></thead>
      <tbody>
        <tr><td><strong>STADA Arzneimittel</strong></td><td>&#x20AC;4.1bn</td><td>&#x20AC;886M</td><td><strong>11.3&#xD7;</strong></td><td>CapVest, Sep 2025 (&#x20AC;10bn EV)</td><td>European specialty pharma + OTC, multi-country platform</td></tr>
        <tr><td><strong>Zentiva</strong></td><td>&#x20AC;1.7bn</td><td>&#x20AC;400M</td><td><strong>10.3&#xD7;</strong></td><td>GTCR, 2025 (&#x20AC;4.8bn EV)</td><td>Pan-European branded generics, cardiology focus</td></tr>
        <tr><td><strong>Krka (listed)</strong></td><td>&#x20AC;2.2bn</td><td>nm</td><td><strong>11.5&#xD7;</strong></td><td>Public, Ljubljana SE</td><td>European branded generics, CEE/CIS exposure</td></tr>
        <tr><td><strong>Karo Healthcare</strong></td><td>&#x20AC;1.1bn</td><td>&#x20AC;250M</td><td><strong>10.5&#xD7;</strong></td><td>EQT exit Sep 2025 (&#x20AC;2.6bn)</td><td>Consumer and OTC healthcare, Nordic/European</td></tr>
        <tr style="background:#EAF0FA;font-weight:600;"><td><strong>Recordati SPC (Year 5 est.)</strong></td><td>&#x20AC;1,632M</td><td>&#x20AC;540M</td><td><strong>9&#x2013;12&#xD7;</strong></td><td>Model range: bear 9&#xD7;, base 11&#xD7;, bull 12&#xD7;</td><td>Branded specialty, urology + cardio + GI, 30+ countries</td></tr>
      </tbody>
    </table>
    <p style="font-size:10.5px;color:var(--g400);margin-top:8px;font-style:italic;">Recordati SPC is not a generics business &#x2014; its branded products command higher margins (33% EBITDA vs 22% for STADA). The appropriate comparable is STADA&#x2019;s specialty pharma segment or Karo Healthcare, both of which cleared 10&#x2013;11&#xD7; in recent transactions, supporting a base case exit of 11&#xD7; with upside to 12&#xD7; in the bull case and a floor of 9&#xD7; in a compressed market environment.</p>
  </div>

  <!-- FRANCHISE-BY-FRANCHISE SOTP TABLE -->
  <h3 style="font-family:'EB Garamond',serif;font-size:19px;color:var(--navy);margin-bottom:12px;">Sum-of-the-Parts Sale — SPC Franchise by Franchise at Year 5</h3>
  <p style="font-size:12.5px;color:var(--g600);margin-bottom:14px;line-height:1.65;">Selling the SPC division as five separate assets to five specialist strategic buyers unlocks a blended multiple of approximately 10.9&#xD7; versus 10&#xD7; for a single block sale &#x2014; a &#x20AC;465M premium. The urology franchise attracts the highest multiple because Eligard is an oncology asset with durable cash flows and patent-protected upside. The cough and cold/OTC/Russia-CIS business attracts the lowest multiple given its geopolitical and currency risk.</p>
  <table class="s" style="margin-bottom:22px;">
    <thead><tr><th>Franchise</th><th>Year 5 Revenue</th><th>EBITDA Margin</th><th>EBITDA</th><th>Multiple Range</th><th>Exit EV</th><th>Strategic Buyers</th></tr></thead>
    <tbody>
      <tr><td><strong>Urology &amp; Uro-oncology</strong><br><span style="font-size:10.5px;color:var(--g400);">Eligard, Urorec, Avodart/Combodart</span></td><td>&#x20AC;490M</td><td>38%</td><td>&#x20AC;186M</td><td>11&#x2013;14&#xD7;</td><td><strong>&#x20AC;2,325M</strong></td><td>AstraZeneca, Ferring, GSK, AbbVie</td></tr>
      <tr><td><strong>Cardiovascular (branded)</strong><br><span style="font-size:10.5px;color:var(--g400);">Zanidip, Livazo, Vazkepa, Seloken</span></td><td>&#x20AC;490M</td><td>35%</td><td>&#x20AC;171M</td><td>10&#x2013;12&#xD7;</td><td><strong>&#x20AC;1,885M</strong></td><td>Servier, Menarini, Bayer</td></tr>
      <tr><td><strong>Gastrointestinal</strong><br><span style="font-size:10.5px;color:var(--g400);">Rx and OTC prescription products</span></td><td>&#x20AC;245M</td><td>30%</td><td>&#x20AC;73M</td><td>9&#x2013;11&#xD7;</td><td><strong>&#x20AC;734M</strong></td><td>Norgine, Takeda GI, Tillotts</td></tr>
      <tr><td><strong>Cough &amp; Cold / OTC / CIS</strong><br><span style="font-size:10.5px;color:var(--g400);">Russia, Turkey, CIS operations (7% of sales)</span></td><td>&#x20AC;245M</td><td>25%</td><td>&#x20AC;61M</td><td>7&#x2013;9&#xD7;</td><td><strong>&#x20AC;490M</strong></td><td>Haleon, Sanofi Consumer, STADA</td></tr>
      <tr><td><strong>Other / Rest-of-World</strong><br><span style="font-size:10.5px;color:var(--g400);">North Africa, APAC, LatAm tail</span></td><td>&#x20AC;163M</td><td>30%</td><td>&#x20AC;49M</td><td>8&#x2013;10&#xD7;</td><td><strong>&#x20AC;441M</strong></td><td>Dr Reddy&#x2019;s, Cipla, local players</td></tr>
      <tr class="tr"><td><strong>Total SPC (Sum of Parts)</strong></td><td>&#x20AC;1,632M</td><td>33%</td><td><strong>&#x20AC;540M</strong></td><td>10.9&#xD7; blended</td><td><strong>&#x20AC;5,875M</strong></td><td>9% premium vs block sale</td></tr>
    </tbody>
  </table>

  <!-- US IPO OPTION FOR WHOLE GROUP -->
  <h3 style="font-family:'EB Garamond',serif;font-size:19px;color:var(--navy);margin-bottom:12px;">What a US Nasdaq Listing Looks Like &#x2014; For the Residual SPC Entity</h3>
  <div class="cgrid" style="margin-bottom:24px;">
    <div class="cc">
      <div class="ct">SPC as a US-Listed Specialty Pharma Company</div>
      <div class="cs">SPC&#x2019;s branded, cash-generative profile fits the US specialty pharma investor base well &#x2014; think Prestige Consumer Healthcare or Jazz Pharmaceuticals rather than rare disease biotech</div>
      <table class="s mt16">
        <thead><tr><th>US Comparable</th><th>Profile</th><th>EV/EBITDA</th></tr></thead>
        <tbody>
          <tr><td><strong>Jazz Pharmaceuticals</strong></td><td>Branded specialty, sleep/CNS/oncology, Europe-anchored</td><td>9&#x2013;11&#xD7;</td></tr>
          <tr><td><strong>Prestige Consumer Healthcare</strong></td><td>OTC branded consumer health, stable cash flows</td><td>10&#x2013;12&#xD7;</td></tr>
          <tr><td><strong>Perrigo (specialty only)</strong></td><td>European OTC and Rx, multi-country</td><td>8&#x2013;10&#xD7;</td></tr>
          <tr><td><strong>Pacira Biosciences</strong></td><td>Branded specialty, non-opioid pain, urology adjacency</td><td>9&#x2013;11&#xD7;</td></tr>
          <tr style="background:#EAF0FA;"><td><strong>Recordati SPC (model range)</strong></td><td>European branded specialty, cardiovascular/urology/GI</td><td><strong>9&#x2013;12&#xD7;</strong></td></tr>
        </tbody>
      </table>
      <p style="font-size:11px;color:var(--g400);margin-top:8px;">A US listing of SPC would likely price at 10&#x2013;11&#xD7; in the base case &#x2014; consistent with European branded specialty pharma trade sale comparables and in line with the 9&#x2013;12&#xD7; model range. SPC lacks a US commercial presence, so a US listing premium is unlikely. A strategic trade sale to a European pharma acquirer is the recommended exit path.</p>
    </div>
    <div class="cc">
      <div class="ct">Preferred Exit Route by Franchise</div>
      <div class="cs">Each SPC sub-business has a natural home &#x2014; the carve-out thesis maximises value by matching each asset to its optimal buyer</div>
      <table class="s mt16">
        <thead><tr><th>Franchise</th><th>Best Exit Route</th><th>Why</th></tr></thead>
        <tbody>
          <tr><td><strong>Urology</strong></td><td>Strategic trade sale</td><td>Eligard + oncology premium; AZ and Ferring both want European urology scale</td></tr>
          <tr><td><strong>Cardiovascular</strong></td><td>Strategic trade sale</td><td>Zanidip is a trophy branded asset; Servier or Menarini would pay 11&#x2013;12&#xD7;</td></tr>
          <tr><td><strong>GI</strong></td><td>Strategic trade sale</td><td>Norgine or Tillotts would pay 9&#x2013;11&#xD7; for European GI scale</td></tr>
          <tr><td><strong>OTC / Russia / Turkey</strong></td><td>Regional strategic / PE</td><td>Haleon or STADA; or sell Turkey plant and Russia operations separately</td></tr>
          <tr><td><strong>RRD (Year 2&#x2013;3)</strong></td><td>Strategic trade sale</td><td>Novo Nordisk, Roche, Novartis want rare disease platform access</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- RETURN COMPARISON: BLOCK vs SOTP vs IPO -->
  <div class="cc" style="margin-bottom:24px;">
    <div class="ct">Exit Route Returns — IRR Comparison (Base Case: RRD at 18&#xD7; Year 3)</div>
    <div class="cs">Total equity &#x20AC;7,133M invested at Year 0 &#x2014; RRD sold Year 3 &#x2014; SPC exit Year 5 (trade sale or IPO) &#x2014; SPC exit multiple range: 9&#xD7; bear, 11&#xD7; base, 12&#xD7; bull</div>
    <div class="cw" style="height:220px;"><canvas id="ipoChart"></canvas></div>
  </div>

  <div class="rgrid" style="margin-bottom:0;">
    <div class="sc base" style="border-color:var(--g200);">
      <div class="sch" style="background:var(--navy);"><h3>Block Sale</h3><span class="sct">SPC sold as one unit · 10&#xD7; Year 5</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">RRD sale Year 3 (to co-investor)</span><span class="ssv">+&#x20AC;5,229M</span></div>
        <div class="ss2"><span class="ssl">SPC block sale Year 5 (10&#xD7; &#xD7; &#x20AC;540M)</span><span class="ssv">+&#x20AC;2,877M</span></div>
        <div class="ss2"><span class="ssl">Total co-investor proceeds</span><span class="ssv">&#x20AC;8,106M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi">1.31&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv">7.6%</span></div>
        <div class="ss2"><span class="ssl">Verdict</span><span class="ssv">Simplest to execute</span></div>
      </div>
    </div>
    <div class="sc base">
      <div class="sch"><h3>SOTP Sale</h3><span class="sct">5 franchises to 5 buyers · 10.9&#xD7; blended</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">RRD sale Year 3</span><span class="ssv">+&#x20AC;5,229M</span></div>
        <div class="ss2"><span class="ssl">SPC SOTP Year 5&#x2013;6 (blended 10.9&#xD7;)</span><span class="ssv">+&#x20AC;3,124M</span></div>
        <div class="ss2"><span class="ssl">Total co-investor proceeds</span><span class="ssv">&#x20AC;8,353M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi">1.35&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv">8.1%</span></div>
        <div class="ss2"><span class="ssl">Verdict</span><span class="ssv">+&#x20AC;465M vs block · +0.5pp IRR</span></div>
      </div>
    </div>
    <div class="sc" style="border-color:var(--g200);">
      <div class="sch" style="background:#2A5A3A;"><h3>RRD US Nasdaq IPO</h3><span class="sct">RRD only listed · SPC sold separately</span></div>
      <div class="scb">
        <div class="ss2"><span class="ssl">RRD IPO Year 3 (17&#xD7;, staged exit)</span><span class="ssv">+&#x20AC;2,634M (Yrs 3&#x2013;5)</span></div>
        <div class="ss2"><span class="ssl">SPC block sale Year 5</span><span class="ssv">+&#x20AC;2,877M</span></div>
        <div class="ss2"><span class="ssl">Total co-investor proceeds</span><span class="ssv">&#x20AC;8,652M</span></div>
        <div class="ss2"><span class="ssl">MOIC</span><span class="ssv hi">1.40&#xD7;</span></div>
        <div class="ss2"><span class="ssl">IRR</span><span class="ssv">7.7%</span></div>
        <div class="ss2"><span class="ssl">Verdict</span><span class="ssv">Higher MOIC, retains Isturisa upside</span></div>
      </div>
    </div>
  </div>

  <div style="background:var(--navy);border-radius:8px;padding:22px 24px;margin-top:22px;">
    <div style="font-family:'EB Garamond',serif;font-size:18px;color:var(--gold);margin-bottom:10px;">The Recommended Path</div>
    <p style="font-size:13px;color:rgba(255,255,255,.75);line-height:1.75;">The highest IRR comes from selling the SPC franchises separately to specialist strategic buyers &#x2014; a 0.5pp uplift over a block sale for &#x20AC;465M of additional proceeds. Urology and cardiovascular both have natural homes at large European pharma companies willing to pay 11&#x2013;13&#xD7; for high-quality branded cash flows. The OTC and Russia/Turkey business is the most challenging to exit and should be sold early to a consumer healthcare acquirer (Haleon, Sanofi) or regional PE platform. CVC has executed more than 25 corporate carve-outs and has the execution capability to run five parallel processes. The recommended structure is therefore: RRD trade sale to a global strategic buyer in Year 2 to 3 at 18&#x2013;22&#xD7; EBITDA, followed by a disciplined franchise-by-franchise SPC exit programme completed by Year 5 to 6.</p>
  </div>
</div>
</div>


<div class="panel" id="p-risks">
<div class="pi">
  <div class="ey">Risk Factors</div>
  <h2 class="st">Principal Risks and Mitigants</h2>
  <div class="dv"></div>
  <p class="ss">A summary of the key risks in this co-investment. Each is assessed for severity relative to the deal structure and accompanied by the primary mitigant available to the sponsor and co-investor group.</p>
  <div class="rg">
    <div class="rc high"><div class="rh"><div class="rt">RRD Sale Execution Risk</div><span class="rl rhi">High</span></div><div class="rdesc">The entire investment thesis depends on successfully separating and selling the rare disease division at a premium multiple. Failure to find a buyer at 15× or above within a four-year window would materially reduce returns and extend the hold period on a business generating strong cash flow but lacking the pure-play valuation premium.</div><div class="rmit">Mitigant: The SPC business has a meaningful pipeline of pending approvals and lifecycle management opportunities that underpin the geographic expansion thesis. Vazkepa (icosapent ethyl), licensed from Amarin in mid-2025 for European cardiovascular markets, is in launch phase across multiple countries. Inrebic (fedratinib), acquired rights in 2025 for myelofibrosis treatment, adds to the rare disease-adjacent portfolio. Cardicor replacement revenues are expected to come from the Cardiovascular pipeline and new country rollouts of existing products including Zanidip and Urorec. The SPC business generates &#x20AC;559M of annual free cash flow at the group level, providing capital to fund new market entry without requiring external financing. In the hold period, geographic expansion into Central and Eastern Europe and the Middle East is a tangible, management-guided strategy that supports the 2% annual growth assumption across all three scenarios.</div></div>
    <div class="rc med"><div class="rh"><div class="rt">Isturisa Commercial Execution</div><span class="rl rme">Medium</span></div><div class="rdesc">Isturisa is the primary driver of the rare disease division's exit valuation. A shortfall against the greater than €1.2bn peak sales target would compress the exit multiple materially and delay the RRD sale timeline.</div><div class="rmit">Mitigant: The FDA label was expanded in April 2025 to cover all Cushing's syndrome patients. The lead competitive drug, relacorilant, was rejected by the FDA in December 2025. Approximately 1,400 net active US patients were on treatment at year-end 2025 with accelerating uptake confirmed in the second half of the year.</div></div>
    <div class="rc med"><div class="rh"><div class="rt">Regulatory and Drug Pricing Risk</div><span class="rl rme">Medium</span></div><div class="rdesc">EU health technology assessment regulation and national reimbursement negotiations could compress rare disease drug pricing in Germany and France, reducing divisional EBITDA ahead of the exit and compressing the achievable multiple.</div><div class="rmit">Mitigant: Rare disease drug designation provides strong pricing protection. No single rare disease drug accounts for more than 50% of divisional revenue, providing meaningful diversification against single-product pricing risk.</div></div>
    <div class="rc med"><div class="rh"><div class="rt">Leverage and Interest Coverage</div><span class="rl rme">Medium</span></div><div class="rdesc">Post-close debt of &#x20AC;5,982M at 6.0&#xD7; entry EBITDA generates annual interest of &#x20AC;299M, covered 3.3&#xD7; by Year 1 EBITDA. While this provides adequate headroom, it is tighter than a conventional investment grade structure. Rising European rates would increase the variable-rate portion of the debt cost. Broader macro headwinds &#x2014; potential US tariff impacts on pharmaceutical imports, a stronger euro compressing USD-denominated revenue translation, and slowing European growth &#x2014; could compress EBITDA while interest costs remain fixed, narrowing coverage ratios in Years 4&#x2013;5 post-RRD when only SPC revenue remains.</div><div class="rmit">Mitigant: EBITDA covers interest at 3.3&#xD7; in Year 1 across all three scenarios, and 2.9&#xD7; at the post-RRD low point in the bear case &#x2014; well above typical covenant floors of 1.5&#xD7;. After the RRD sale, &#x20AC;2,991M of debt is repaid from proceeds, halving interest to &#x20AC;150M and reducing leverage materially. Rate hedging on the new term loan is expected at close to cap exposure to EURIBOR movements.</div></div>
    <div class="rc med"><div class="rh"><div class="rt">Italian Political Sensitivity</div><span class="rl rme">Medium</span></div><div class="rdesc">Recordati is a nationally significant Italian listed company. A foreign-led take-private could attract scrutiny or a golden share review, potentially delaying close beyond the H2 2026 target date.</div><div class="rmit">Mitigant: CVC has owned Recordati since 2018 with no political friction. The Italian management team is fully retained, domestic manufacturing is unaffected and the company remains a major Italian employer throughout.</div></div>
    <div class="rc low"><div class="rh"><div class="rt">Specialty Pharma Maturation</div><span class="rl rlo">Lower</span></div><div class="rdesc">The specialty pharma division faces patent expirations and generic competition through 2026 to 2030, which could reduce free cash flow generation and compress the SPC exit multiple.</div><div class="rmit">Mitigant: SPC is valued at 9 to 11× EBITDA in the model, already reflecting this risk. Generic pressure at SPC would be more than offset by a successful and accelerated rare disease division sale at premium multiples.</div></div>
  </div>
</div>
</div>

</div><!-- end body -->

<footer>
  <div class="fb">Recordati <span>S.p.A.</span> · Co-Investment</div>
  <div class="fd">This document is confidential and prepared for sophisticated institutional investors only. It does not constitute financial projections, an offer to sell or a solicitation to invest. Share price &#x20AC;50.00 as of 17 April 2026; offer price &#x20AC;52.00 per share (4.0% premium to last close). Enterprise Value &#x20AC;12.24bn per PitchBook (market cap &#x20AC;10.20bn + total debt &#x20AC;2.467bn &#x2212; cash &#x20AC;429M = &#x20AC;12,240M; 17 April 2026). Entry EV/EBITDA: 12.35&#xD7; on FY2025 EBITDA &#x20AC;991.1M (matches PitchBook normalised EV/EBITDA of 12.35&#xD7;). Forward EV/EBITDA: 12.18&#xD7; (PitchBook). Total transaction value &#x20AC;13,115M. Sources: new co-investor equity &#x20AC;2,131M (&#x20AC;2,110M free float + &#x20AC;21M transaction costs, 30% of fees) + Rossini rollover &#x20AC;5,002M (&#x20AC;4,953M + &#x20AC;49M transaction costs, 70% of fees) + existing debt refinanced &#x20AC;2,467M + new term loan &#x20AC;3,515M. Total equity &#x20AC;7,133M (54%); total debt &#x20AC;5,982M (46%) at 5.0% flat. Annual interest &#x20AC;299M Years 1&#x2013;3; &#x20AC;150M Years 4&#x2013;5 after &#x20AC;2,991M (50% of debt) repaid from RRD proceeds. Entry debt/EBITDA: 6.0&#xD7;; Year 1 EBITDA/interest: 3.3&#xD7;. Returns on total equity &#x20AC;7,133M (timed cash flows): base 1.50&#xD7; / 9.1% IRR; bull 2.12&#xD7; / 16.4%; bear 0.95&#xD7; / (1.3)%. RRD = 59% of group EBITDA and revenue; SPC = 41%. RRD FY2025 revenue &#x20AC;1,081M (GlobeNewswire, 17 Feb 2026). FX headwind FY2025: &#x20AC;64.2M (&#x2212;2.7%); FY2026 guidance: &#x2212;3.5%. Relacorilant received a Complete Response Letter from the FDA for Cushing&#x2019;s syndrome in December 2025; separately approved for platinum-resistant ovarian cancer (Lifyorli&#x2122;) in March 2026 &#x2014; a distinct indication that does not compete with Isturisa. All figures as of 17 April 2026.</div>
</footer>

<script>
Chart.defaults.font.family="'DM Sans',sans-serif";
Chart.defaults.font.size=12;
Chart.defaults.color='#6C6C64';
const N='#0D1B3E',NM='#1A2F5A',NL='#243F78',G='#B8964E',GR='#A8A89E',GL='#E2E2DE',GRN='#1B5E42',RED='#C0392B';
const C={};

function initCharts(id){
  if(id==='valuation'&&!C.ev){
    C.ev=new Chart(document.getElementById('evChart'),{
      type:'bar',
      data:{labels:['FY2020','FY2021','FY2022','FY2023','FY2024','Apr 2026'],
        datasets:[
          {label:'Recordati EV/EBITDA',data:[18.0,21.8,15.0,15.9,13.8,12.35],
            backgroundColor:[NL,NL,NL,NL,NL,RED],borderWidth:0,borderRadius:3,yAxisID:'y',order:2},
          {label:'European Pharma Peer Avg',data:[16.5,17.2,14.8,14.2,13.5,13.5],
            type:'line',borderColor:G,backgroundColor:'transparent',pointBackgroundColor:G,
            borderWidth:2,pointRadius:4,yAxisID:'y',order:1,tension:0.3}
        ]},
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>` ${c.dataset.label}: ${c.raw}×`}}},
        scales:{x:{grid:{display:false}},y:{grid:{color:GL},ticks:{callback:v=>`${v}×`},min:0,max:26}}}
    });
  }
  if(id==='financials'&&!C.rev){
    C.rev=new Chart(document.getElementById('revChart'),{type:'bar',
      data:{labels:['FY2021','FY2022','FY2023','FY2024','FY2025'],
        datasets:[{label:'Rare Disease',data:[503,692,840,879,1081],backgroundColor:N,borderWidth:0},
                  {label:'Specialty Pharma',data:[980,1080,1190,1449,1478],backgroundColor:G,borderWidth:0}]},
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>` ${c.dataset.label}: €${c.raw}M`}}},
        scales:{x:{stacked:true,grid:{display:false}},y:{stacked:true,grid:{color:GL},ticks:{callback:v=>`€${v}M`}}}}
    });
    C.ebitda=new Chart(document.getElementById('ebitdaChart'),{type:'bar',
      data:{labels:['FY2021','FY2022','FY2023','FY2024','FY2025'],
        datasets:[{label:'EBITDA (€M)',data:[545,644,727,866,991],backgroundColor:N,borderWidth:0,yAxisID:'y',order:2},
                  {label:'Margin (%)',data:[36.7,36.9,37.1,37.5,37.8],type:'line',borderColor:G,
                   backgroundColor:'transparent',pointBackgroundColor:G,borderWidth:2,pointRadius:4,yAxisID:'y1',order:1}]},
      options:{responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false}},
        scales:{x:{grid:{display:false}},y:{grid:{color:GL},ticks:{callback:v=>`€${v}M`},min:0,max:1200},
                y1:{position:'right',grid:{display:false},ticks:{callback:v=>`${v}%`},min:34,max:42}}}
    });
  }
  if(id==='captable'&&!C.cap){
    const cd={labels:['CVC Capital Partners','Free Float','PSP Investments','StepStone Group','AlpInvest Partners'],
              values:[31.5,53.2,6.0,5.5,3.8],colors:[N,'#E2E2DE',NM,NL,'#4A6FA5']};
    C.cap=new Chart(document.getElementById('capChart'),{type:'doughnut',
      data:{labels:cd.labels,datasets:[{data:cd.values,backgroundColor:cd.colors,borderWidth:2,borderColor:'#fff',hoverOffset:6}]},
      options:{responsive:true,maintainAspectRatio:false,cutout:'62%',
               plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>` ${c.label}: ${c.raw}%`}}}}
    });
    const leg=document.getElementById('capLeg');
    cd.labels.forEach((l,i)=>{
      leg.innerHTML+=`<div style="display:flex;align-items:center;gap:8px;font-size:12px;"><span style="width:9px;height:9px;border-radius:50%;background:${cd.colors[i]};flex-shrink:0;"></span><span style="flex:1;color:#3A3A34;">${l}</span><span style="font-weight:500;color:#0D1B3E;">${cd.values[i]}%</span></div>`;
    });
  }
  if(id==='deal'&&!C.sotp){
    C.sotp=new Chart(document.getElementById('sotpChart'),{type:'bar',
      data:{labels:['Entry EV','RRD (18×)','SPC (10×)','SOTP Total','Value Gap'],
        datasets:[{data:[11.97,7.8,4.8,12.6,0.63],backgroundColor:[GR,N,G,GRN,RED],borderWidth:0,borderRadius:3}]},
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>` €${c.raw}bn`}}},
        scales:{x:{grid:{display:false}},y:{grid:{color:GL},ticks:{callback:v=>`€${v}bn`},min:0,max:16}}}
    });
  }
  if(id==='market'&&!C.mkt){
    const yrs=['2023','2024','2025E','2026E','2027E','2028E','2029E','2030E','2031E','2032E','2033E'];
    const md=yrs.map((_,i)=>parseFloat((135.9*Math.pow(1.138,i)).toFixed(1)));
    md[0]=135.9;md[1]=154.6;
    C.mkt=new Chart(document.getElementById('marketChart'),{type:'line',
      data:{labels:yrs,datasets:[{data:md,borderColor:N,backgroundColor:'rgba(13,27,62,.07)',fill:true,
            borderWidth:2,pointBackgroundColor:N,pointRadius:4,tension:0.3}]},
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>` $${c.raw}bn`}}},
        scales:{x:{grid:{display:false}},y:{grid:{color:GL},ticks:{callback:v=>`$${v}bn`}}}}
    });
  }
  if(id==='returns'&&!C.irr){
    C.irr=new Chart(document.getElementById('irrChart'),{type:'bar',
      data:{labels:['Bear 12×\n(no expansion)','Base 18×\nRRD exit','Bull 22×\nRRD exit'],
        datasets:[{label:'Year 2 Sale',data:[null,58,78],backgroundColor:NL,borderWidth:0,borderRadius:3},
                  {label:'Year 3 Sale',data:[null,36,55],backgroundColor:N,borderWidth:0,borderRadius:3},
                  {label:'Year 5 Sale',data:[11,22,34],backgroundColor:G,borderWidth:0,borderRadius:3}]},
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.raw?` ${c.dataset.label}: ~${c.raw}% IRR`:' Not applicable'}}},
        scales:{x:{grid:{display:false}},y:{grid:{color:GL},ticks:{callback:v=>`${v}%`},min:0,max:90}}}
    });
  }
  if(id==='ipo'&&!C.ipo){
    C.ipo=new Chart(document.getElementById('ipoChart'),{
      type:'bar',
      data:{
        labels:['Block Sale (10×)','SOTP Sale (10.9×)','RRD Nasdaq IPO + SPC Block'],
        datasets:[
          {label:'MOIC',data:[1.31,1.35,1.40],backgroundColor:[NL,N,GRN],borderWidth:0,borderRadius:3,yAxisID:'y1'},
          {label:'IRR %',data:[7.6,8.1,7.7],backgroundColor:['rgba(184,150,78,.7)','rgba(184,150,78,.9)',G],borderWidth:0,borderRadius:3,yAxisID:'y2'}
        ]
      },
      options:{responsive:true,maintainAspectRatio:false,
        plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.datasetIndex===0?` MOIC: ${c.raw}×`:` IRR: ${c.raw}%`}}},
        scales:{
          x:{grid:{display:false}},
          y1:{position:'left',grid:{color:'#E2E2DE'},ticks:{callback:v=>`${v}×`},min:1.0,max:1.6,title:{display:true,text:'MOIC',color:'#6C6C64',font:{size:10}}},
          y2:{position:'right',grid:{display:false},ticks:{callback:v=>`${v}%`},min:5,max:11,title:{display:true,text:'IRR',color:'#B8964E',font:{size:10}}}
        }}
    });
  }
}

function showSc(id,btn){
  document.querySelectorAll('.sp').forEach(p=>p.classList.remove('on'));
  document.querySelectorAll('.stab').forEach(b=>b.classList.remove('on'));
  document.getElementById('sc-'+id).classList.add('on');
  btn.classList.add('on');
}

document.querySelectorAll('.tb').forEach(btn=>{
  btn.addEventListener('click',()=>{
    const id=btn.dataset.tab;
    document.querySelectorAll('.tb').forEach(b=>b.classList.toggle('on',b.dataset.tab===id));
    document.querySelectorAll('.panel').forEach(p=>p.classList.toggle('on',p.id==='p-'+id));
    window.scrollTo({top:0,behavior:'instant'});
    initCharts(id);
  });
});
</script>
</body>
</html>
