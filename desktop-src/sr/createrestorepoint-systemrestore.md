---
title: Método CreateRestorePoint da classe SystemRestore
description: Cria um ponto de restauração.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Restauração do sistema do método CreateRestorePoint
- CreateRestorePoint método de restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455289"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>Método CreateRestorePoint da classe SystemRestore

Cria um ponto de restauração.

Esse método é o equivalente programável da função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descrição* \[ do no\]
</dt> <dd>

A descrição a ser exibida para que o usuário possa identificar facilmente um ponto de restauração. O comprimento máximo de uma cadeia de caracteres ANSI é MAX \_ desc. O comprimento máximo de uma cadeia de caracteres Unicode é o máximo \_ desc \_ W. Para obter mais informações, consulte [texto de descrição do ponto de restauração](restore-point-description-text.md).

</dd> <dt>

*RestorePointType* \[ no\]
</dt> <dd>

O tipo de ponto de restauração. Esse membro pode ser um dos valores a seguir.



| Tipo de ponto de restauração                                                                                                                                                                                                                             | Significado                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> Do <dt>**aplicativo \_ INSTALAR**</dt> <dt>0</dt> </dl>         | Um aplicativo foi instalado.<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> Do <dt>**aplicativo \_ DESINSTALAR**</dt> <dt>1</dt> </dl>   | Um aplicativo foi desinstalado.<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Dispositivo \_ do \_Instalação do driver**</dt> <dt>10</dt> </dl> | Um driver de dispositivo foi instalado.<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modificar \_ CONFIGURAÇÕES**</dt> <dt>12</dt> </dl>                    | Um aplicativo teve recursos adicionados ou removidos.<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Cancelado \_ OPERAÇÃO**</dt> <dt>13</dt> </dl>        | Um aplicativo precisa excluir o ponto de restauração criado. Por exemplo, um aplicativo usaria esse sinalizador quando um usuário cancelar uma instalação.<br/> |



 

</dd> <dt>

*EventType* \[ no\]
</dt> <dd>

O tipo do evento. Esse membro pode ser um dos valores a seguir.



| Tipo de evento                                                                                                                                                                                                                                                      | Significado                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Iniciar \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>102</dt> </dl> | Uma alteração do sistema foi iniciada. Uma chamada aninhada subsequente não cria um novo ponto de restauração. <br/> As chamadas subsequentes devem usar encerrar \_ alteração do sistema aninhada \_ \_ , não \_ alteração do sistema final \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Iniciar \_ \_Alteração do sistema**</dt> <dt>100</dt> </dl>                       | Uma alteração do sistema foi iniciada. <br/> Uma chamada subsequente deve usar A \_ alteração do sistema final \_ , e não encerrar a \_ alteração do sistema aninhado \_ \_ .<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fim \_ \_ \_ Alteração de sistema aninhada**</dt> <dt>103</dt> </dl>       | Uma alteração do sistema foi encerrada.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fim \_ \_Alteração do sistema**</dt> <dt>101</dt> </dl>                             | Uma alteração do sistema foi encerrada.<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o valor de retorno será S \_ OK. Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.

## <a name="remarks"></a>Comentários

* * Windows 8: * *

Uma nova chave do Registro permite que os desenvolvedores de aplicativos alterem a frequência da criação do ponto de restauração.

Os aplicativos devem criar essa chave para usá-la porque ela não existirá no sistema. O seguinte será aplicado por padrão se a chave não existir. Se um aplicativo chamar o método **CreateRestorePoint** para criar um ponto de restauração, o Windows ignorará a criação desse novo ponto de restauração se quaisquer pontos de restauração tiverem sido criados nas últimas 24 horas. O método **CreateRestorePoint** retorna **S \_ OK**.

Os desenvolvedores podem escrever aplicativos que criam o valor **DWORD** **SystemRestorePointCreationFrequency** na chave do registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração. O valor dessa chave do registro pode alterar a frequência da criação do ponto de restauração.

Se o aplicativo chamar **CreateRestorePoint** para criar um ponto de restauração e o valor da chave do registro for 0, a restauração do sistema não ignorará a criação do novo ponto de restauração.

Se o aplicativo chamar **CreateRestorePoint** para criar um ponto de restauração e o valor da chave do registro for o inteiro N, a restauração do sistema ignorará a criação de um novo ponto de restauração se qualquer ponto de restauração tiver sido criado nos N minutos anteriores.

## <a name="examples"></a>Exemplos


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                         |
| Namespace<br/>                | \\Padrão raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





