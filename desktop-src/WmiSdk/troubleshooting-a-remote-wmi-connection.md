---
description: As seções a seguir descrevem os problemas comuns que os desenvolvedores podem ter com a criação de uma conexão WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Solucionando problemas de conexão WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761209"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Solucionando problemas de conexão WMI remota

As seções a seguir descrevem os problemas comuns que os desenvolvedores podem ter com a criação de uma conexão WMI remota.

As seções a seguir são discutidas neste tópico:

-   [Acesso ao DCOM negado](#dcom-access-denied)
-   [Falha ao conectar](#failure-to-connect)
-   [A conexão WMI atingiu o tempo limite](#wmi-connection-timed-out)
-   [Tópicos relacionados](#related-topics)

## <a name="dcom-access-denied"></a>Acesso ao DCOM negado

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas
</dt> <dd>

a conexão falhou com o erro "DCOM Access Denied", juntamente com o valor decimal-2147024891 ou hex value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo
</dt> <dd>

O DCOM pode não estar configurado para permitir uma conexão WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução
</dt> <dd>

Você pode definir as configurações do DCOM para o WMI usando o utilitário de configuração do DCOM (**DCOMCnfg.exe**) encontrado em **Ferramentas administrativas** no **painel de controle**. Esse utilitário expõe as configurações que permitem que determinados usuários se conectem ao computador remotamente por meio do DCOM. Os membros do grupo Administradores têm permissão para se conectar remotamente ao computador por padrão. Com esse utilitário, você pode definir a segurança para iniciar, acessar e configurar o serviço WMI.

Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Falha ao conectar

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas
</dt> <dd>

Você não pode se conectar ao WMI em um sistema remoto.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo
</dt> <dd>

Você pode estar tentando se conectar a um sistema que não dá suporte a WMI. Não há suporte para as seguintes conexões entre as versões do sistema operacional:

-   Não é possível se conectar a um computador que esteja executando uma edição inicial, básica ou Home.

Como alternativa, você pode estar tentando se conectar a um namespace que requer uma conexão criptografada, uma que exija um nível de autenticação de `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** ou a privacidade do PCT do nível de autenticação **RPC \_ \_ \_ \_ \_ C**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução
</dt> <dd>

Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md), [protegendo clientes e provedores do C++](securing-c---clients-and-providers.md)ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>A conexão WMI atingiu o tempo limite

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas
</dt> <dd>

Sua conexão WMI atinge o tempo limite.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo
</dt> <dd>

Devido a problemas de atraso na rede, o computador simplesmente não pode responder no tempo.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução
</dt> <dd>

Ao se conectar ao WMI por meio de uma chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), você pode definir o sinalizador **wbemConnectFlagUseMaxWait** (Scripting) ou o **\_ sinalizador WBEM \_ Connect \_ use \_ Max \_ Wait** no valor C++ para 128 (0x80) para impor um tempo limite de dois (2) minutos na chamada.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



