---
title: Classe SystemRestore
description: Fornece métodos para desabilitar e habilenciar o monitoramento, listar pontos de restauração disponíveis e iniciar uma restauração no sistema local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Classe SystemRestore Restauração do Sistema
- Classe SystemRestore Restauração do Sistema , descrita
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca781f960f51c8f7804d56f3b2f5531517c3f16505f40dd48d442857fa58bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967985"
---
# <a name="systemrestore-class"></a>Classe SystemRestore

Fornece métodos para desabilitar e habilenciar o monitoramento, listar pontos de restauração disponíveis e iniciar uma restauração no sistema local.

## <a name="syntax"></a>Sintaxe

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Membros

A **classe SystemRestore** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe SystemRestore** tem esses métodos.



| Método                                                             | Descrição                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Cria um ponto de restauração.<br/>                         |
| [**Desabilitar**](disable-systemrestore.md)                           | Desabilita o monitoramento em uma unidade específica.<br/>       |
| [**Habilitar**](enable-systemrestore.md)                             | Habilita o monitoramento em uma unidade específica.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Recupera o status da última restauração do sistema.<br/> |
| [**Restaurar**](restore-systemrestore.md)                           | Inicia uma restauração do sistema.<br/>                      |



 

### <a name="properties"></a>Propriedades

A **classe SystemRestore** tem essas propriedades.

<dl> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A hora em que a alteração de estado ocorreu.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A descrição a ser exibida para que o usuário possa identificar facilmente um ponto de restauração. O comprimento máximo de uma cadeia de caracteres ANSI é MAX \_ DESC. O comprimento máximo de uma cadeia de caracteres Unicode é MAX \_ DESC \_ W. Para obter mais informações, consulte [Restaurar texto de descrição do ponto](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tipo do evento. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**BEGIN \_ ALTERAÇÃO \_ \_ ANINHADA DO SISTEMA**</dt> <dt>102</dt> </dl> | Uma alteração do sistema foi iniciada. Uma chamada aninhada subsequente não cria um novo ponto de restauração. <br/> As chamadas subsequentes devem usar END \_ NESTED \_ SYSTEM \_ CHANGE, não END \_ SYSTEM \_ CHANGE.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**BEGIN \_ ALTERAÇÃO \_ DO SISTEMA**</dt> <dt>100</dt> </dl>                       | Uma alteração do sistema foi iniciada.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**END \_ ALTERAÇÃO \_ \_ ANINHADA DO SISTEMA**</dt> <dt>103</dt> </dl>       | Uma alteração do sistema foi encerrada.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**END \_ ALTERAÇÃO \_ DO SISTEMA**</dt> <dt>101</dt> </dl>                             | Uma alteração do sistema foi encerrada.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tipo de ponto de restauração. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**APLICATIVO \_ INSTALAR**</dt> <dt>0</dt> </dl>         | Um aplicativo foi instalado.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**APLICATIVO \_ DESINSTALAR**</dt> <dt>1</dt> </dl>   | Um aplicativo foi desinstalado.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**CANCELADO \_ OPERAÇÃO**</dt> <dt>13</dt> </dl>        | Um aplicativo precisa excluir o ponto de restauração que ele criou. Por exemplo, um aplicativo usaria esse sinalizador quando um usuário cancela uma instalação. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**DISPOSITIVO \_ INSTALAÇÃO \_ DO DRIVER**</dt> <dt>10</dt> </dl> | Um driver de dispositivo foi instalado.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**MODIFY \_ CONFIGURAÇÕES**</dt> <dt>12</dt> </dl>                    | Um aplicativo teve recursos adicionados ou removidos.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

O número de sequência do ponto de restauração.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode obter uma lista de pontos de restauração usando o [**método SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) para recuperar uma coleção de **objetos SystemRestore.** Você pode usar as propriedades de classe para identificar o ponto de restauração.

## <a name="examples"></a>Exemplos

O script de exemplo a seguir enumera os pontos de restauração atuais.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                         |
| Namespace<br/>                | Padrão \\ raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Instrumentação de Gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

