---
title: Enumeração de MPTHREAT_CATEGORY (MpClient. h)
description: Categorias de ameaça possíveis.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- recursos do ambiente de Windows herdado de enumeração de MPTHREAT_CATEGORY
- Windows recursos de ambiente herdados do ponteiro de enumeração PMPTHREAT_CATEGORY
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70cfd95de751d51be3ab4b61bc361687738422a6d31c234576e812efcd57bd4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975966"
---
# <a name="mpthreat_category-enumeration"></a>\_Enumeração de categoria MPTHREAT

Categorias de ameaça possíveis.

## <a name="syntax"></a>Syntax

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Constantes

Categoria de ameaça | Descrição
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_ Categoria de ameaça \_ \_ inválida** | A categoria de ameaça não existe ou foi digitada incorretamente.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_ \_ \_ adware de categoria de ameaça** | Um aplicativo potencialmente indesejado que exibe anúncios.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_ \_ \_ spyware de categoria de ameaça** | Malware que transmite informações sobre o dispositivo ou usuário, sem o consentimento ou o conhecimento do usuário.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_ \_ \_ PASSWORDSTEALER de categoria de ameaça** | Um aplicativo que coleta e/ou transmite uma senha para um invasor.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**\_TROJANDOWNLOADER de \_ categoria de ameaça MP \_** | Um cavalo de Troia que baixa malware ou aplicativos potencialmente indesejados para um dispositivo infectado.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_ \_ \_ worm de categoria de ameaça** | Autopropagação de software mal-intencionado que pode se distribuir automaticamente por meio de conexões de rede.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**porta de ameaça do MP \_ \_ \_ Backdoor** | Malware que fornece um meio de ignorar protocolos de segurança e autenticação normais em um dispositivo.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_ \_ \_ REMOTEACCESSTROJAN de categoria de ameaça** | Um cavalo de Troia que fornece acesso remoto a um computador.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**\_cavalo de \_ Troia de categoria de ameaça MP \_** | Software mal-intencionado que se disfarça como um software legítimo.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_ \_ \_ EMAILFLOODER de categoria de ameaça** | Malware o envia um grande volume de email para um destino.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_ \_ \_ KEYLOGGER de categoria de ameaça** | Malware que registra os pressionamentos de teclas do usuário, rouba potencialmente as senhas e outros dados confidenciais.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_ \_ \_ discagem de categoria de ameaça** | Malware que faz chamadas telefônicas não autorizadas, geralmente com tarifas Premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_ \_ \_ MONITORINGSOFTWARE de categoria de ameaça** | Um aplicativo potencialmente indesejado que monitora a atividade do usuário, como o que o usuário digita em seu teclado ou modos de exibição na tela.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_ \_ \_ BROWSERMODIFIER de categoria de ameaça** | Um aplicativo potencialmente indesejado que altera as configurações do navegador da Web sem o consentimento do usuário.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_ \_ \_ cookie de categoria de ameaça** | Os dados que um servidor Web envia para um navegador, permitindo que ele Salve informações sobre o usuário, como configurações de aplicativo Web, em visitas repetidas.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_ \_ \_ BROWSERPLUGIN de categoria de ameaça** | O software que permite que um navegador da Web padrão exiba e execute tipos específicos de conteúdo, como arquivos de mídia, imagens animadas e formulários interativos.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_ \_ \_ AOLEXPLOIT de categoria de ameaça** | Malware que ataca os usuários do serviço de Internet da AOL, frequentemente recuperando senhas ou modificando configurações.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_ \_ \_ NUKER de categoria de ameaça** | Malware criado para falhar em um dispositivo ou deixá-lo menos estável.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_ \_ \_ SECURITYDISABLER de categoria de ameaça** | Malware que desabilita as configurações de segurança ou os produtos.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_ \_ \_ JOKEPROGRAM de categoria de ameaça** | Um aplicativo projetado para amuse ou assustam um usuário, sem realmente prejudicar o dispositivo.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_ \_ \_ HOSTILEACTIVEXCONTROL de categoria de ameaça** | um controle de ActiveX projetado por um invasor para danificar um dispositivo. um controle de ActiveX é um tipo de complemento do navegador específico do Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_ \_ \_ SOFTWAREBUNDLER de categoria de ameaça** | Software que instala outros aplicativos potencialmente indesejados, como adware ou spyware. O contrato de licença do software de agrupamento pode exigir esses outros componentes para funcionar.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_ \_ \_ STEALTHNOTIFIER de categoria de ameaça** | Malware que se conecta a um servidor remoto por meio de uma conexão furtiva para notificar um invasor de que o malware foi instalado.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_ \_ \_ SETTINGSMODIFIER de categoria de ameaça** | Um aplicativo potencialmente indesejado que altera as configurações de um usuário sem o conhecimento ou o consentimento do usuário.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_ \_barra de \_ ferramentas de categoria de ameaça** | Um aplicativo potencialmente indesejado (PUA) que instala uma barra de ferramentas no navegador da Web do usuário; geralmente agrupados com PUA adicionais, como adware.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_ \_ \_ REMOTECONTROLSOFTWARE de categoria de ameaça** | Um aplicativo potencialmente indesejado que fornece acesso remoto a um dispositivo.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_ \_ \_ TROJANFTP de categoria de ameaça** | Um cavalo de Troia que usa um servidor FTP para permitir que um invasor carregue ou baixe arquivos de um dispositivo.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_ \_ \_ POTENTIALUNWANTEDSOFTWARE de categoria de ameaça** | Também conhecido como *aplicativo potencialmente indesejado* ou *pua*; software que pode se comportar de uma maneira excessivamente invasiva, que o usuário pode não ter esperado ou totalmente consentido.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_ \_ \_ ICQEXPLOIT de categoria de ameaça** | Um cavalo de Troia que ataca o serviço de mensagens do ICQ, muitas vezes recuperando senhas ou violando as configurações.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_ \_ \_ TROJANTELNET de categoria de ameaça** | Um cavalo de Troia que instala um servidor Telnet no computador de um usuário sem o conhecimento ou o consentimento do usuário.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_ \_ \_ exploração de categoria de ameaça** | Código mal-intencionado que aproveita uma vulnerabilidade em um dispositivo ou sistema.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_ \_ \_ FILESHARINGPROGRAM de categoria de ameaça** | Um aplicativo potencialmente indesejado que abre um dispositivo para o compartilhamento ponto a ponto dos arquivos do dispositivo.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_ \_ferramenta de \_ \_ criação \_ de malware de categoria de ameaça** | Um aplicativo que pode gerar automaticamente arquivos mal-intencionados.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_ Categoria de ameaça \_ \_ \_ \_ software de controle remoto** | Um aplicativo potencialmente indesejado que permite acesso remoto a um dispositivo.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_ \_ \_ ferramenta de categoria de ameaça** | Um utilitário que ajuda um invasor a executar ações mal-intencionadas em um dispositivo.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_ \_DENIALOFSERVICE de \_ cavalo \_ de Troia de categoria de ameaça** | Um cavalo de Troia que foi projetado para enviar um grande volume de solicitações de rede a um destino como parte de um ataque de DoS (negação de serviço).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_ \_instalador de \_ cavalo \_ de Troia de categoria de ameaça** | Um cavalo de Troia que baixa e instala malware ou aplicativos potencialmente indesejados em um destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_ \_MASSMAILER de \_ cavalo \_ de Troia de categoria de ameaça** | Um cavalo de Troia que envia um grande volume de email para um destino, destinado a sobrecarregar a caixa de entrada do destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_ \_MONITORINGSOFTWARE de \_ cavalo \_ de Troia de categoria de ameaça** | Um cavalo de Troia que monitora a atividade do usuário, como o que o usuário digita em seu teclado ou exibições na tela.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_ \_PROXYSERVER de \_ cavalo \_ de Troia de categoria de ameaça** | Um servidor proxy instalado por um cavalo de Troia, fornecendo o que parece ser uma conexão ininterrupta com a Internet, permitindo o acesso não autorizado ao dispositivo infectado.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_ \_ \_ vírus de categoria de ameaça** | Malware que Replica, normalmente, infectando outros arquivos no sistema, permitindo assim a execução do código de malware e sua propagação quando esses arquivos são ativados.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_ Categoria de ameaça \_ \_ conhecida** | Uma ameaça de malware não especificada.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_ Categoria de ameaça \_ \_ desconhecida** | Uma ameaça de malware não especificada que ainda não foi definida.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_ Categoria de ameaça \_ \_ spp** | tecnologia antipirataria que exige que cada instalação de um produto Windows seja ativada com a Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_ \_ \_ comportamento da categoria de ameaça** | Um tipo de detecção com base em ações de arquivo que geralmente são associadas a atividades mal-intencionadas.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_ \_ \_ VULNERABILTIY de categoria de ameaça** | Qualquer fraqueza, processo administrativo ou atividade que torna um dispositivo suscetível a explorar por uma ameaça.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_ \_ \_ política de categoria de ameaça** | Um conjunto de regras definidas por um administrador, que controla recursos em desktops e dispositivos móveis, como atualizações de software.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 8 (somente aplicativos da área de trabalho) |
| Servidor mínimo com suporte | Windows Server 2012 (somente aplicativos da área de trabalho) |
| Cabeçalho | MpClient. h |
