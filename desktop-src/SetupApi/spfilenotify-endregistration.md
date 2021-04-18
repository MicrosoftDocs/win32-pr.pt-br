---
description: Ao usar a diretiva RegisterDlls INF para Autoregistro de DLLs, os chamadores de SetupInstallFromInfSection podem receber notificações em cada arquivo conforme ele é registrado ou cancelado.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Mensagem de SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756362"
---
# <a name="spfilenotify_endregistration-message"></a>\_Mensagem de ENDregistro do SPFILENOTIFY

Ao usar a diretiva **RegisterDlls** inf para Autoregistro de DLLs, os chamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) podem receber notificações em cada arquivo conforme ele é registrado ou cancelado. Para enviar uma notificação de **\_ endregistro do SPFILENOTIFY** para uma rotina de retorno de chamada uma vez depois de registrar ou cancelar o registro de um arquivo, inclua \_ o REGISTERCALLBACKAWARE mais giratório do \_ regsvr no parâmetro *flags* de **SetupInstallFromInfSection**. Para enviar a notificação de cancelamento de registro, inclua \_ o REGISTERCALLBACKAWARE mais giratório e o UNREGSVR mais giratório \_ no parâmetro *flags* .

A rotina de retorno de chamada especificada pelo parâmetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve ser o tipo de [retorno de \_ \_ chamada de arquivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Defina o parâmetro de *contexto* para o mesmo *contexto* especificado em **SetupInstallFromInfSection**. Defina o parâmetro de *notificação* como **SPFILENOTIFY \_ endregistro**.


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura de status de controle de registro do SP que contém informações sobre o arquivo que está sendo registrado ou não registrado. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) O membro **cbSize** deve ser definido como o tamanho da estrutura. **Filename** deve ser definido como o caminho totalmente qualificado do arquivo que está sendo registrado. **Win32Error** deve ser definido como um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) indicando um código de erro estendido. **FailureCode** deve ser definido como um dos códigos de falha válidos indicando o resultado do registro. Para obter códigos de falha válidos, consulte [**status do controle de registro do SP \_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Se o arquivo estiver sendo registrado, *param2* deverá ser definido como um ponteiro para um valor diferente de zero. Se o registro do arquivo estiver sendo cancelado, *param2* deverá ser definido como um ponteiro para zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Depois de receber a notificação, a função de retorno de chamada pode retornar um dos valores a seguir.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_anular FILEOP**</dt> </dl> | Pare de processar a seção INF.<br/>     |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Continue processando a seção INF.<br/> |
| <dl> <dt>**\_ignorar arquivo**</dt> </dl>    | Continuar processando a seção INF<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)
</dt> </dl>

 

