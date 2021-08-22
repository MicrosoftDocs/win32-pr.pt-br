---
description: Descreve os aspectos virtuais de um sistema virtual por meio de um conjunto de propriedades específicas da virtualização. O CIM \_ VirtualSystemSettingData também é usado como a classe de nível superior das configurações do sistema virtual.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1caed7797343eac9babd320af42fd6c9aaaffeff054211cc55bda0d437582d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068486"
---
# <a name="cim_virtualsystemsettingdata-class"></a>Classe CIM \_ VirtualSystemSettingData

Descreve os aspectos virtuais de um sistema virtual por meio de um conjunto de propriedades específicas da virtualização. **CIM \_ VirtualSystemSettingData** também é usado como a classe de nível superior de configurações do sistema virtual.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ VirtualSystemSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ VirtualSystemSettingData** tem essas propriedades.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ação a ser tomada para o sistema virtual quando o software executado pelo sistema virtual falhar. As falhas resolvidas por essa propriedade incluem apenas aquelas detectáveis pela plataforma de host, como uma condição de estado de espera não interruptível.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Reiniciar** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Reverter para o instantâneo** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ação a ser tomada para o sistema virtual quando o host é desligado.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Desligar** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Salvar estado** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Desligamento** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ação a ser tomada no sistema virtual quando o host é iniciado.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Reiniciar se estiver ativo anteriormente** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Sempre inicialização** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O atraso para a ação de inicialização. Esse valor é uma variante de intervalo do **tipo de dados datetime.**

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de sequência para ativação do sistema virtual quando o sistema host é iniciado. Um número inferior indica a ativação anterior. Se uma ou mais configurações mostrarem o mesmo valor, a sequência dependerá da implementação. Um valor de "0" indica que a sequência depende da implementação.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo do diretório em que as informações sobre a configuração do sistema virtual são armazenadas. O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**Configurationfile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho relativo do arquivo em que as informações sobre a configuração do sistema virtual são armazenadas. O caminho relativo é anexado ao valor da **propriedade ConfigurationDataRoot.** O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ID exclusiva da configuração do sistema virtual.

> [!Note]  
> **ConfigurationID** é diferente da **InstanceID** e é atribuída pela implementação a um sistema virtual ou uma configuração de sistema virtual. **ConfigurationID** não é uma chave e o mesmo valor pode ocorrer para mais de uma instância.

 

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a configuração do sistema virtual foi criada.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo relativo do diretório em que as informações de log do sistema virtual são armazenadas. O caminho relativo é anexado ao valor da **propriedade ConfigurationDataRoot.** O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**Observações**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém observações fornecidas pelo usuário relacionadas ao sistema virtual.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo em que as informações relacionadas à recuperação do sistema virtual são armazenadas. O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho relativo do diretório em que as informações sobre instantâneos do sistema virtual são armazenadas. O caminho relativo é anexado ao valor da **propriedade ConfigurationDataRoot.** O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho relativo do diretório em que as informações relacionadas de suspensão sobre o sistema virtual são armazenadas. O caminho relativo é anexado ao valor da **propriedade ConfigurationDataRoot.** O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo relativo do diretório em que os arquivos de permuta do sistema virtual são armazenados. O caminho relativo é anexado ao valor da **propriedade ConfigurationDataRoot.** O formato dessa propriedade é um URI baseado no RFC 2079.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome exclusivo para o sistema dentro da plataforma de virtualização. **VirtualSystemIdentifier** não é o nome do host atribuído à instância do sistema operacional em execução no sistema virtual, nem é um endereço IP ou endereço MAC atribuído a qualquer uma de suas portas de rede.

O **VirtualSystemIdentifier** pode conter regras específicas de implementação, como padrões simples ou uma expressão regular que pode ser interpretada pela implementação ao definir **VirtualSystemIdentifier**.

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo do sistema virtual.

> [!Note]  
> Se o tipo de sistema virtual for desconhecido, esse valor deverá ser definido como "DMTF:unknown".

 

Essa propriedade é formatada usando o seguinte formato ABNF (Formulário de Naur de Backus Aumentados) :

vs-type = dmtf-value/other-org-value/legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;

O valor do formato ABNF acima é:

-   *dmtf-value um*   valor da propriedade definido por DMTF e é definido na descrição dessa propriedade.
-   *other-org-value é*   um valor de propriedade definido por uma entidade de negócios diferente de DMTF e não está definido na descrição dessa propriedade.
-   *legacy-value*   um valor da propriedade definido por uma entidade de negócios diferente de DMTF e não está definido na descrição dessa propriedade. Esses valores são permitidos, mas recomendados para serem preterido ao longo do tempo.
-   *defineing-org*   um identificador para a entidade de negócios que define o tipo de sistema virtual. Ele deve incluir um nome protegido por direitos autorais, marcas comerciais ou um nome exclusivo pertencente à entidade de negócios. Ele não deve ser "DMTF" e não deve conter dois-pontos.
-   *org-vs-type um*   identificador para o tipo de sistema virtual dentro da entidade de negócios que define. Ele deve ser exclusivo em defining-org. org-vs-type pode usar qualquer caractere permitido para cadeias de caracteres CIM, exceto o seguinte: U0000-U001F (controles Unicode C0), U0020 (espaço), U007F (controles Unicode C0) ou controles U0080-U009F (Unicode C1).
-   Se houver a necessidade de estruturar o valor em segmentos, os segmentos deverão ser separados por um único dois-pontos.
-   Os valores dessa propriedade devem ser processados de forma sensível a casos. Eles devem ser processados programaticamente, em vez de serem um nome de exibição e devem ser curtos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> </dl>

 

 




