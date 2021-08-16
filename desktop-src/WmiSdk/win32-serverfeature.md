---
description: A classe Win32 \_ ServerFeature representa os recursos instalados em um computador que executa Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Classe Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312133"
---
# <a name="win32_serverfeature-class"></a>Classe Win32 \_ ServerFeature

\[A **classe Win32 \_ ServerFeature** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use as Classes de Provedor [serverManager Deploymentprovider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]

A **classe Win32 \_ ServerFeature** representa os recursos instalados em um computador que executa Windows Server.

Essa classe pode ser usada por desenvolvedores e administradores que precisam automatizar o processo de determinar os recursos instalados em um conjunto de computadores de servidor. As instâncias dessa classe não estão disponíveis em computadores cliente.

## <a name="syntax"></a>Sintaxe

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ ServerFeature** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ServerFeature win32** tem essas propriedades.

<dl> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**Chave**](key-qualifier.md), [**Não \_ Nulo**](optional-qualifiers.md)
</dt> </dl>

ID do recurso do servidor. A lista a seguir mostra os valores possíveis da propriedade ID:



Valor

Nome

1

[Servidor de Aplicativos](/windows)

2

Servidor Web (IIS)

3

[Serviços de Mídia de Fluxo Contínuo](/windows)

5

Servidor de Fax

6

Serviços de Arquivo e iSCSI<br/> [alteração de nome](/windows)<br/>

7

Serviços de impressão e documentos<br/> [alteração de nome](/windows)<br/>

8

[Serviços de Federação do Active Directory (AD FS)](/windows)

9

Active Directory Lightweight Directory Services

10

Active Directory Domain Services

11

[Serviços UDDI](/windows)<br/>

12

[Servidor DHCP](/windows)

13

[Servidor DNS](/windows)

14

Network Policy and Access Services

16

Serviços de Certificados do Active Directory

17

Active Directory Rights Management Services

18

[Serviços de área de trabalho remota](/windows)<br/> [alteração de nome](/windows)<br/>

19

Windows Deployment Services

20

Hyper-v

21

[Windows Server Update Services](/windows)

33

[Clustering de failover](/windows)

34

[Balanceamento de Carga de Rede](/windows)

36

[Recursos do .NET Framework 3.5.1](/windows)<br/> [alteração de nome](/windows)<br/>

37

[Gerenciador de recursos de sistema do Windows](/windows)

38

Serviço de LAN sem fio

39

[Windows Recursos de backup do servidor](/windows)

40

Servidor WINS

41

Serviço de Ativação de Processos do Windows

42

[Assistência Remota](/windows)

43

Serviços TCP/IP Simples

44

[Cliente Telnet](/windows)

45

[Servidor Telnet](/windows)

46

[Subsistema para aplicativos baseados em Unix](/windows)

47

RPC por proxy HTTP

48

Servidor SMTP

49

Enfileiramento de Mensagens

51

[Banco de Dados Interno do Windows](/windows)

52

[Armazenamento Gerente para SANs](/windows)

53

Monitor de Porta LPR

55

[Internet Storage Name Server](/windows)

57

[Multipath I/O](/windows)

58

Cliente TFTP

59

[Serviços SNMP](/windows)

60

[Gerenciador de Armazenamento removível](/windows)

61

Criptografia de Unidade de Disco BitLocker

62

[Serviços para o sistema de arquivos de rede](/windows)

63

Cliente de Impressão via Internet

64

[Protocolo de resolução de nome par](/windows)

65

Kit de administração do Gerenciador de conexões

66

[Windows PowerShell](/windows)<br/>

67

[Ferramentas Administrativas do Servidor Remoto](/windows)

68

[Quality Windows Audio-Video Experience](/windows)

69

[Gerenciamento de Política de Grupo](/windows)

71

[Indexing Service](/windows)

72

[Gerenciador de Recursos de Servidor de Arquivos (FSRM)](/windows)

73

Compressão diferencial remota

310

Serviços de tinta e manuscrito<br/>

320

[Ferramentas de Migração do Windows Server](/windows)<br/>

321

[Extensão IIS WinRM](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[Console de gerenciamento DirectAccess](/windows)<br/>

335

[BITS (serviço de Transferência Inteligente em Segundo Plano)](/windows)<br/>

338

[Visualizador XPS](/windows)<br/>

339

[Windows Biometric Framework](/windows)<br/>

340

Suporte a WoW64<br/>

351

[Windows PowerShell ISE (Ambiente de Script Integrado)](/windows)<br/>

352

Windows TIFF IFilter<br/>

404

[Windows Server Update Services](/windows)

409

[Servidor de Gerenciamento de Endereço IP (IPAM)](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Serviço Windows Search](/windows)

438

[Cliente NFS](/windows)

441

[Desbloqueio de Rede do BitLocker](/windows)

442

[Extensão do IIS do Management OData](/windows)

450

[Serviços avançados do .NET Framework 4.5](/windows)

466

[Recursos do .NET Framework 4.5](/windows)

468

[Acesso remoto](/windows)<br/>

477

[Interfaces do usuário e infraestrutura](/windows)

478

[Ferramentas e Infraestrutura de Gerenciamento Gráfico](/windows)

481

[Serviços de Arquivo e Armazenamento](/windows)

485

[Experiência do Windows Server Essentials](/windows)

488

[Direct Play](/windows)

Serviços de Arquivos – Serviços de Função (6)

Valor

Nome

100

[Sistema de Arquivos Distribuído](/windows)

101

Namespace de DFS

102

Replicação do DFS

103

[Serviço de Replicação de Arquivos](/windows)

104

[Gerenciador de Recursos de Servidor de Arquivos (FSRM)](/windows)

105

[Serviços para sistema de arquivos de rede](/windows)

106

[Armazenamento de instância única](/windows)

107

[Serviço Windows Search](/windows)

108

[Indexing Service](/windows)

255

Servidor de Arquivos

350

BranchCache para arquivos de rede

431

[Servidor para NFS](/windows)<br/>

434

[Serviço de Agente VSS de Servidor de Arquivos](/windows)<br/>

435

[Servidor de destino iSCSI](/windows)<br/>

436

[Eliminação de Duplicação de Dados](/windows)<br/>

437

[provedor de Armazenamento de destino iSCSI (provedores de hardware VDS e VSS)](/windows)

486

[Pastas de trabalho](/windows)

Serviços de função de AD DS (10)

Valor

Nome

110

[Controlador de Domínio do Active Directory](/windows)

111

[Gerenciamento de identidade para UNIX](/windows)

112

[Servidor para serviços de informações de rede](/windows)

113

[Sincronização de senha](/windows)

294

[Ferramentas Administrativas do Servidor Remoto](/windows)

Streaming de mídia – serviços de função (3)

Valor

Nome

120

[Windows Servidor de mídia](/windows)

121

[Administração baseada na Web](/windows)

122

[Agente de log](/windows)

ADFS – serviços de função (8)

Valor

Nome

125

[Serviços de Federação do Active Directory (AD FS)](/windows)

126

[Política de Serviço de Federação](/windows)

127

[Agentes Web do AD FS](/windows)

128

[Agente de Reconhecimento de Declaração](/windows)

129

[Agente baseado no token do Windows](/windows)

Serviços de função de Serviços de Área de Trabalho Remota (18)

Valor

Nome

130

Host de Sessão de Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

131

[Licenciamento de Área de Trabalho Remota](/windows)<br/> [alteração de nome](/windows)<br/>

132

Gateway de Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

133

Agente de Conexão de Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

134

Acesso via Web à Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

322

Host de Virtualização de área de trabalho remota<br/>

Serviços de função de Host de Virtualização de Área de Trabalho Remota (322)

Valor

Nome

325

[Serviços principais](/windows)<br/>

327

[Gráficos virtuais Área de Trabalho Remota](/windows)<br/>

Serviços de função de Serviços de Impressão e Documentos (7)

Valor

Nome

135

Servidor de Impressão

136

Impressão via Internet

137

Serviço de impressão LPD

328

[Servidor de Digitalização Distribuída](/windows)<br/>

Servidor Web (IIS)-serviços de função (2)

Valor

Nome

140

Servidor Web

141

Recursos comuns de HTTP

142

Conteúdo Estático

143

Documento padrão

144

Pesquisa no diretório

145

Erros HTTP

146

Redirecionamento de HTTP

147

Desenvolvimento do aplicativo

148

ASP.NET

149

Extensibilidade .NET

150

ASP

151

CGI

152

Extensões ISAPI

153

Filtros ISAPI

154

Server Side Includes

155

Integridade e diagnóstico

156

Log HTTP

157

Ferramentas de log

158

Monitor de Solicitações

159

Rastreamento

160

Registro em log personalizado

161

Log de ODBC

162

Segurança

163

Autenticação Básica

164

Autenticação do Windows

165

Autenticação Digest

166

Autenticação de mapeamento de certificado de cliente

167

Autenticação de mapeamento de certificado do cliente IIS

168

Autorização de URL

169

Filtragem de Solicitações

170

Restrições de IP e domínio

171

Desempenho

172

Compactação de Conteúdo Estático

173

Compactação de Conteúdo Dinâmico

174

Ferramentas de gerenciamento

175

Console de Gerenciamento IIS

176

Ferramentas e scripts de gerenciamento do IIS

177

Management Service

178

Compatibilidade de gerenciamento do IIS 6

179

Compatibilidade de Metabase do IIS 6

180

Compatibilidade de WMI do IIS 6

181

Ferramentas de script do IIS 6

182

Console de gerenciamento do IIS 6

183

Serviço de Publicação FTP<br/>

184

Servidor FTP

185

Console de Gerenciamento do FTP<br/>

314

Publicação de WebDAV

316

Serviço de FTP<br/>

317

Extensibilidade de FTP<br/>

336

Núcleo da Web Hospedável do IIS<br/>

413

[ASP.NET 4,5](/windows)

414

[Extensibilidade 4.5 do .NET](/windows)

445

[appialization](/windows)

446

[Suporte Centralizado a Certificado SSL](/windows)

447

[Protocolo WebSocket](/windows)

En fila de mensagens – Recursos (49)

Valor

Nome

190

Serviços de Ensuamento de Mensagens

191

Servidor de En ensuamento de mensagens

192

Integração de Serviços de Diretório

193

Gatilhos de en fila de mensagens

194

Suporte a HTTP

195

Serviço de roteamento

196

[Windows 2000 Client Support](/windows)<br/>

197

Proxy DCOM do Serviço de Enfileiramento de Mensagens

228

Suporte a multicasting

Serviços de Certificados do Active Directory - Serviços de Função (16)

Valor

Nome

200

Autoridade de certificação

201

Registro na Web de Autoridade de Certificação

202

Respondente Online

204

Serviço de Inscrição do Dispositivo de Rede

318

[Serviço Web de Registro de Certificado](/windows)<br/>

319

[Serviço Web de Política de Registro de Certificado](/windows)<br/>

Política de rede e Serviços do Access - Serviços de Função (14)

Valor

Nome

205

[Servidor de Políticas de Rede](/windows)

206

[VPN](#vpn)

207

[Controle remoto Serviços do Access](/windows)

208

[Roteiros](#routing)

210

[Autoridade de Registro de Integridade](/windows)

250

[Protocolo de autorização de credencial de host](/windows)

Serviços UDDI – Serviços de Função (11)

Valor

Nome

215

[Aplicativo Web UDDI Services](/windows)<br/>

216

[Banco de dados UDDI Services](/windows)<br/>

Windows Serviço de Ativação de Processo – Serviços de Função (41)

Valor

Nome

217

API de configuração

218

Ambiente .NET

219

Modelo de processo

.NET Framework 3.5.1 – Recursos (36)

Valor

Nome

220

.NET Framework 3.5.1<br/> [alteração de nome](/windows)<br/>

221

Ativação de WCF

222

Ativação HTTP

223

Ativação não HTTP

227

Visualizador XPS<br/>

Serviços SNMP – Recursos (59)

Valor

Nome

224

[Serviço SNMP](/windows)

225

[Provedor WMI SNMP](/windows)

Serviços de Aplicativos – Serviços de Função

Valor

Nome

230

[.NET Framework 3.5.1](/windows)<br/> [alteração de nome](/windows)<br/>

231

[Suporte do Servidor Web (IIS)](/windows)

232

[Acesso à rede COM+](/windows)

233

[Compartilhamento de porta TCP](/windows)

234

[Windows Suporte ao Serviço de Ativação de Processo](/windows)

235

[Ativação HTTP](/windows)

236

[Ativação do En ensuamento de mensagens](/windows)

237

[Ativação TCP](/windows)

238

[Ativação de pipes nomeados](/windows)

239

[Transações distribuídas](/windows)

240

[Transações remotas de entrada](/windows)

241

[Transações remotas de saída](/windows)

242

[Transações automáticas do WS](/windows)

353

[Extensões do Servidor de Aplicativos para .NET 4.0](/windows)<br/>

Windows Serviços de Implantação – Função (19)

Valor

Nome

251

Servidor de Implantação

252

Servidor de Transporte

Active Directory Rights Management Services - Serviços de Função (17)

Valor

Nome

253

Servidor de Gerenciamento de Direitos do Active Directory

254

Suporte à Federação de Identidade

Ferramentas de Administração de Servidor Remoto (67)

Valor

Nome

256

[Ferramentas de administração de funções](/windows)

257

[Ferramentas de AD DS](/windows)<br/> [alteração de nome](/windows)<br/>

258

[AD LDS Snap-Ins e Command-Line ferramentas](/windows)<br/> [alteração de nome](/windows)<br/>

259

Ferramentas de Serviços de Certificados do Active Directory

260

[Network Policy and Access Services](/windows)

261

Serviços de Impressão e Documentos Ferramentas de Serviços de Impressão e Documentos<br/> [alteração de nome](/windows)<br/>

262

[Active Directory Rights Management Services](/windows)

263

[Ferramentas de Serviços de Área de Trabalho Remota](/windows)<br/> [alteração de nome](/windows)<br/>

264

Windows Ferramentas dos Serviços de Implantação

265

[Ferramentas de administração do recurso](/windows)

266

BitLocker Drive Encryption Tools

267

Ferramentas de extensões de servidor BITS

268

[Ferramentas de cluster de failover](/windows)

269

Ferramentas de Balanceamento de Carga de Rede

270

Ferramentas do servidor SMTP

273

[Ferramentas de servidor DNS](/windows)

277

Ferramentas de serviços de arquivo

278

Sistema de Arquivos Distribuído Ferramentas de Sistema de Arquivos Distribuído

279

Ferramentas do Gerenciador de Recursos de Servidor de Arquivos

280

[Serviços para ferramentas do sistema de arquivos de rede](/windows)

281

Ferramentas do Servidor Web (IIS)

284

[Host da Sessão da Área de Trabalho Remota Ferramentas de Host da Sessão da Área de Trabalho Remota](/windows)<br/> [alteração de nome](/windows)<br/>

285

Ferramentas de gateway Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

286

Ferramentas de licenciamento Área de Trabalho Remota<br/> [alteração de nome](/windows)<br/>

288

Ferramentas de servidor de fax

290

Ferramentas de servidor WINS

291

[Ferramentas dos serviços UDDI](/windows)<br/>

292

Ferramentas de autoridade de certificação

293

Ferramentas de Respondente Online

297

[Ferramentas de Servidor para NIS](/windows)

299

[Snap-ins AD DS e Ferrramentas de linha de comando](/windows)<br/> [alteração de nome](/windows)<br/>

300

[Centro Administrativo do Active Directory](/windows)

301

Ferramentas do Hyper-V

323

[Visualizador de senha de recuperação do BitLocker](/windows)<br/>

326

[BitLocker Drive Encryption Administration Utilities](/windows)<br/>

329

[Ferramentas AD DS e AD LDS](/windows)<br/>

330

Centro Administrativo do Active Directory<br/>

331

[Módulo do Active Directory para o Windows PowerShell](/windows)<br/>

337

[Ferramentas do agente de Conexão de Área de Trabalho Remota](/windows)<br/>

410

[cliente Gerenciamento de Endereço IP (IPAM)](/windows)

450

[Módulo Hyper-V para o Windows PowerShell](/windows)

462

[Active Directory Rights Management Services Ferramentas](/windows)

465

[ferramenta de gerenciamento de compartilhamento e Armazenamento](/windows)

471

[Ferramentas de Gerenciamento de Acesso Remoto](/windows)

472

[Módulo de Acesso Remoto para o Windows PowerShell](/windows)

473

[GUI de acesso remoto e ferramentas de Command-Line](/windows)

474

[Ferramentas do Windows Server Update Services](/windows)

476

[Ferramentas do diagnosticador de licenciamento Área de Trabalho Remota](/windows)

479

[Ferramentas SNMP](/windows)

480

[Ferramentas de ativação de volume](/windows)

Windows Backup do servidor-recursos (39)

Valor

Nome

296

[Backup do Windows Server](/windows)

297

[Ferramentas de linha de comando](/windows)

Serviços de Reconhecimento de Manuscrito-recursos (310)

Valor

Nome

311

[Suporte à tinta](/windows)<br/>

312

[Reconhecimento de manuscrito](/windows)<br/>

Serviço de Transferência Inteligente em Segundo Plano (BITS)-recursos (335)

Valor

Nome

54

Extensão do Servidor IIS

332

[Compact Server](/windows)<br/>

Suporte WOW64-recursos (340)

Valor

Nome

341

[WoW64](#wow64)<br/>

342

[WoW64 para .NET Framework 2,0 e Windows PowerShell](/windows)<br/>

343

[WoW64 para .NET Framework 2,0](/windows)<br/>

344

[WoW64 para PowerShell](/windows)<br/>

345

[WoW64 para .NET Framework 3,0 e 3,5](/windows)<br/>

346

[WoW64 para serviços de impressão](/windows)<br/>

347

[WoW64 para clustering de failover](/windows)<br/>

348

[WoW64 para editor de método de entrada](/windows)<br/>

349

[WoW64 para subsistema para aplicativos baseados em UNIX](/windows)<br/>

Interfaces do usuário e serviços de função de infraestrutura (447)

Valor

Nome

35

[Experiência Desktop](/windows)

99

[Shell gráfico do servidor](/windows)

Windows Server Update Services-recursos (404)

Valor

Nome

405

[Cmdlets do PowerShell e API](/windows)

406

[SQL Server Conectividade](/windows)

407

[Serviços do WSUS](/windows)

408

[Console de gerenciamento de interface do usuário](/windows)

449

[Conectividade de WID](/windows)

Windows PowerShell-recursos (417)

Valor

Nome

411

[Windows PowerShell mecanismo 2,0](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Windows PowerShell Web Access](/windows)

1000

[serviço de Desired State Configuration Windows PowerShell](/windows)

.NET Framework 4,5-recursos (418)

Valor

Nome

419

[.NET Framework 4,5 estendido](/windows)

420

[Serviços do WCF](/windows)

421

[Ativação HTTP](/windows)

422

[Ativação do MSMQ (enfileiramento de mensagens)](/windows)

423

[Ativação de Pipe Nomeado](/windows)

424

[Ativação TCP](/windows)

425

[Compartilhamento de porta TCP](/windows)

429

[ASP.NET 4,5](/windows)

Acesso remoto-função (468)

Valor

Nome

469

[DirectAccess e VPN (RAS)](/windows)

470

[Roteiros](#routing)

arquivo e serviços de Armazenamento-função (481)

Valor

Nome

482

[Serviços de Armazenamento](/windows)

484

[Ferramentas de gerenciamento de cluster de failover](/windows)



 

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome de exibição do recurso do servidor, como "servidor de arquivos", "Servidor de Impressão" ou "experiência desktop".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número de ID do recurso do servidor pai. Essa propriedade será 0 se o recurso representado pela instância atual da classe não tiver um recurso pai.

</dd> </dl>

## <a name="remarks"></a>Comentários

leia a [visão geral técnica do Windows Server 2008 Gerenciador do Servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) para saber mais sobre os recursos do servidor.

as empresas que não usam software de gerenciamento que relata recursos do servidor, como System Center Operations Manager com pacotes de gerenciamento instalados, podem obter essas informações consultando a classe **Win32 \_ ServerFeature** .

Você pode usar os recursos de comunicação remota do WMI ou do WinRM para obter informações de recursos de servidor de servidores remotos. Para obter mais informações sobre conexões DCOM remotas do WMI, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md). Para obter mais informações sobre o WinRM, confira Gerenciamento Remoto do Windows.

Windows Server 2012: o **Win32 \_ ServerFeature** foi preterido. Para acessar as informações de recurso do Windows Server programaticamente, você pode usar os [cmdlets Gerenciador do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Servidor de aplicativos
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Serviços de Mídia de Streaming
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Serviços de Federação do Active Directory (AD FS)
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Servidor DHCP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Servidor DNS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Serviços de Área de Trabalho Remota
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clustering de failover
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Balanceamento de carga de rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>recursos do .NET Framework 3.5.1
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Gerenciador de recursos do sistema
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Recursos de backup do servidor
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistência remota
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Cliente Telnet
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Servidor Telnet
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsistema para aplicativos baseados em UNIX
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Banco de Dados Interno do Windows
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Armazenamento Manager para SANs
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>servidor de nome do Internet Armazenamento
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Serviços SNMP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Serviços para sistema de arquivos de rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocolo de resolução de nome de par
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Ferramentas de Administração de Servidor Remoto
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>qualidade Windows experiência em vídeo de áudio
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gerenciamento de Política de Grupo
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Serviço de indexação
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>FSRM (Gerenciador de recursos de servidor de arquivos)
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Ferramentas de migração do servidor
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gerenciamento do DirectAccess
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Serviço de Transferência Inteligente em Segundo Plano (BITS)
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Suporte a WoW64
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Serviços de atualização de servidor do Windows
</dt> <dd>

Adicionado

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>servidor Gerenciamento de Endereço IP (IPAM)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Serviço de Pesquisa
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Cliente para NFS
</dt> <dd>

Adicionado

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Desbloqueio de rede do BitLocker
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extensão do IIS do Management OData
</dt> <dd>

Adicionado

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework serviços avançados 4,5
</dt> <dd>

Adicionado

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>recursos do .NET Framework 4,5
</dt> <dd>

Adicionado

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces do usuário e infraestrutura
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Ferramentas e infraestrutura de gerenciamento gráfico
</dt> <dd>

Adicionado

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>serviços de arquivo e Armazenamento
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Experiência do Server Essentials
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Play direto
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Sistema de Arquivos Distribuído
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Gerenciador de recursos do servidor de arquivos
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Serviços para sistema de arquivos de rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Armazenamento de instância única
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Serviço de Pesquisa
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Serviço de indexação
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>provedor de Armazenamento de destino iSCSI (provedores de hardware VDS e VSS)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de trabalho
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Controlador de Domínio do Active Directory
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gerenciamento de identidade para UNIX
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Servidor para serviços de informações de rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronização de senha
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Ferramentas de Administração
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Servidor de Mídia
</dt> <dd>

Não tem mais suporte.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administração baseada na Web
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente de registro em log
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Serviço de Federação
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Serviço de Federação política de Serviço de Federação
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Agente baseado em token
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Área de Trabalho Remota licenciamento
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Servidor de Política de Rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>Vpn
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Controle remoto Serviços do Access
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Roteamento
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autoridade de Registro de Saúde
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocolo de autorização de credencial de host
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizador XPS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Serviço SNMP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Provedor WMI SNMP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Suporte ao Servidor Web (IIS)
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acesso à rede COM+
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Compartilhamento de porta TCP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Suporte ao Serviço de Ativação de Processo
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Ativação HTTP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Ativação do En ensuamento de mensagens
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Ativação TCP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Ativação de pipes nomeados
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transações distribuídas
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transações remotas de entrada
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transações remotas de saída
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transações automáticas do WS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensões do Servidor de Aplicativos para .NET 4.0
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Ferramentas de Administração de Função
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Ferramentas de AD DS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins e Command-Line ferramentas
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Política de rede e Serviços do Access
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Serviços de Área de Trabalho Remota Ferramentas de Serviços de Área de Trabalho Remota
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Ferramentas de Administração de Recursos
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Ferramentas de clustering de failover
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Ferramentas do Servidor DNS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Serviços para ferramentas do sistema de arquivos de rede
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Ferramentas do Servidor Web (IIS)
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Servidor para NIS Ferramentas de Servidor para NIS
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins e Command-Line ferramentas
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS e AD LDS ferramentas
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Conexão de Área de Trabalho Remota Broker Tools
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Gerenciamento de Endereço IP (IPAM)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo do Hyper-V para Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Ferramenta
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Compartilhar e Armazenamento gerenciamento de dados
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Ferramentas de Gerenciamento de Acesso Remoto
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo acesso remoto para Windows PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>GUI de acesso remoto e ferramentas Command-Line acesso remoto
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Ferramentas
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Área de Trabalho Remota de diagnóstico de licenciamento do Área de Trabalho Remota
</dt> <dd>

Adicionado

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Ferramentas SNMP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Ferramentas de ativação de volume
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Backup do servidor
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Ferramentas de linha de comando
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Suporte a tinta
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconhecimento de manuscrito
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 para .NET Framework 2.0 e PowerShell
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2.0
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3.0 e 3.5
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para Serviços de Impressão
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clustering de failover
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para o Editor de Método de Entrada
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Experiência desktop
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell Gráfico do Servidor
</dt> <dd>

Adicionado

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>Cmdlets da API e do PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Conectividade
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Serviços do WSUS
</dt> <dd>

Adicionado

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Interface do Usuário de Gerenciamento do Interface do Usuário
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Conectividade WID
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell mecanismo 2.0
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Acesso via Web
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Serviço de Windows PowerShell Desired State Configuration
</dt> <dd>

Adicionado

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Estendido
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Serviços WCF
</dt> <dd>

Adicionado

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Ativação HTTP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Ativação do MSMQ (Enqueing de Mensagens)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Ativação de pipe nomeado
</dt> <dd>

Adicionado

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Ativação TCP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Compartilhamento de porta TCP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5
</dt> <dd>

Adicionado

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilidade do .NET 4.5
</dt> <dd>

Adicionado

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess e VPN (RAS)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Roteamento
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Armazenamento Serviços
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Ferramentas de gerenciamento de cluster de failover
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Ferramentas
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inicialização do aplicativo
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Suporte centralizado ao certificado SSL
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente com conhecimento de declarações
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Host da Sessão da Área de Trabalho Remota Ferramentas de Host da Sessão da Área de Trabalho Remota
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocolo WebSocket
</dt> <dd>

não há mais suporte para

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acesso à rede COM+
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Alteração de nome dos Serviços iSCSI e arquivo
</dt> <dd>

Alterado para Serviços de Arquivos

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces do usuário e infraestrutura
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Servidor para NFS
</dt> <dd>

Adicionado

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Serviço de Agente VSS do Servidor de Arquivos
</dt> <dd>

Adicionado

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Servidor de Destino iSCSI
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Desduplicação de dados
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de Trabalho
</dt> <dd>

Removido

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Serviços principais
</dt> <dd>

Adicionado somente para esta versão.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Área de Trabalho Remota gráficos virtuais
</dt> <dd>

Adicionado somente para esta versão

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Acesso remoto
</dt> <dd>

Adicionado

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Serviços UDDI
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Sistema Resource Manager
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Gerenciador de Armazenamento removível
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Serviços de Reconhecimento de Manuscrito
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extensão do IIS do WinRM
</dt> <dd>

Adicionado

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de Gerenciamento do DirectAccess
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Serviço de Transferência Inteligente em Segundo Plano (BITS)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizador XPS
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Estrutura biométrica
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Suporte a WoW64
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell ISE (Ambiente de Script Integrado)
</dt> <dd>

Adicionado

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Serviço de Replicação de Arquivos
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache para arquivos de rede
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de Trabalho
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Servidor de Digitalização Distribuída
</dt> <dd>

Adicionado

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Serviço de Publicação FTP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console de Gerenciamento de FTP
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Serviço FTP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilidade de FTP
</dt> <dd>

Adicionado

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Núcleo Da Web acessível pelo IIS
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Serviço Web de Registro de Certificado
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Serviço Web de Política de Registro de Certificado
</dt> <dd>

Adicionado

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Aplicativo Web UDDI Services
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Banco de dados UDDI Services
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensões do Servidor de Aplicativos para .NET 4.0
</dt> <dd>

Adicionado

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Ferramentas de serviços UDDI
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>utilitários Criptografia de Unidade de Disco BitLocker administração do Criptografia de Unidade de Disco BitLocker
</dt> <dd>

Adicionado

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS e AD LDS ferramentas
</dt> <dd>

Não é mais compatível

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS e AD LDS ferramentas
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro Administrativo do Active Directory
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Módulo do Active Directory para Windows PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Conexão de Área de Trabalho Remota Broker Tools
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 para .NET Framework 2,0 e Windows PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 e 3,5
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para serviços de impressão
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clustering de failover
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para editor de método de entrada
</dt> <dd>

Adicionado

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para subsistema para aplicativos baseados em UNIX
</dt> <dd>

Adicionado

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visualizador de senha de recuperação do BitLocker
</dt> <dd>

Adicionado

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Alteração de nome de Serviços de Impressão e Documentos
</dt> <dd>

Serviços de impressão nomeados para esta versão

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Alteração de nome de Serviços de Área de Trabalho Remota
</dt> <dd>

Serviços de terminal nomeados nesta versão

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>alteração de nome de recursos do .NET Framework 3.5.1
</dt> <dd>

recursos do .NET Framework 3,0 nomeados nesta versão

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Alteração de nome de Host da Sessão da Área de Trabalho Remota
</dt> <dd>

Terminal Server nomeado nesta versão

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Alteração do nome de licenciamento Área de Trabalho Remota
</dt> <dd>

Licenciamento de TS nomeado nesta versão

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Alteração do nome do gateway Área de Trabalho Remota
</dt> <dd>

TS Gateway nomeado nesta versão

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Alteração do nome do agente de Conexão de Área de Trabalho Remota
</dt> <dd>

Agente de Sessão TS nomeado nesta versão

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Alteração de nome de Acesso via Web à Área de Trabalho Remota
</dt> <dd>

Acesso via Web de TS nomeados nesta versão

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>alteração de nome do .NET Framework 3.5.1
</dt> <dd>

(220) denominada recursos do NET FX 3,0 nesta versão

(230) nome do servidor de aplicativos chamado nesta versão

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de AD DS
</dt> <dd>

Ferramentas de Active Directory Domain Services nomeadas nesta versão

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins e Command-Line alteração de nome de ferramentas
</dt> <dd>

Ferramentas de serviços AD LDS nomeadas nesta versão

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Serviços de Impressão e Documentos
</dt> <dd>

Ferramentas de serviços de impressão nomeados nesta versão

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Serviços de Área de Trabalho Remota
</dt> <dd>

Ferramentas de serviços de terminal nomeados nesta versão

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Host da Sessão da Área de Trabalho Remota
</dt> <dd>

Ferramentas de Terminal Server nomeadas nesta versão

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Alteração de nome das ferramentas de gateway Área de Trabalho Remota
</dt> <dd>

Ferramentas de gateway de TS nomeadas nesta versão

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Alteração do nome das ferramentas de licenciamento Área de Trabalho Remota
</dt> <dd>

Ferramentas de Licenciamento TS nomeadas nesta versão

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins e Command-Line alteração de nome de ferramentas
</dt> <dd>

Ferramentas de controlador de domínio Active Directory

</dd> </dl>

## <a name="examples"></a>Exemplos

O script a seguir exibe os nomes de todos os recursos de servidor no computador chamado "FABRIKAM". observe que o computador de destino deve estar executando o Windows server 2008 ou um sistema operacional de servidor posterior.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

