---
description: Ao usar a diretiva RegisterDlls INF para Autoregistro de DLLs, os chamadores de SetupInstallFromInfSection podem receber notificações em cada arquivo conforme ele é registrado ou cancelado.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Mensagem de SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811272"
---
# <a name="spfilenotify_startregistration-message"></a>\_Mensagem SPFILENOTIFY STARTREGISTRATION

Ao usar a diretiva **RegisterDlls** inf para Autoregistro de DLLs, os chamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) podem receber notificações em cada arquivo conforme ele é registrado ou cancelado. Para enviar uma notificação **SPFILENOTIFY \_ STARTREGISTRATION** para a rotina de retorno de chamada uma vez antes de registrar um arquivo, inclua \_ o REGISTERCALLBACKAWARE mais giratório e \_ o regsvr mais giratório no parâmetro *flags* de **SetupInstallFromInfSection**. Para enviar a notificação de cancelamento de registro, inclua \_ o REGISTERCALLBACKAWARE mais giratório e o UNREGSVR mais giratório \_ no parâmetro *flags* .

A rotina de retorno de chamada especificada pelo parâmetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve ser o tipo de [retorno de \_ \_ chamada de arquivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Defina o parâmetro de *contexto* para o mesmo *contexto* especificado em **SetupInstallFromInfSection**. Defina o parâmetro de *notificação* como **SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura de status de controle de registro do SP que contém informações sobre o arquivo que está sendo registrado ou não registrado. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) O membro **cbSize** deve ser definido como o tamanho da estrutura. O membro **filename** deve ser definido como o caminho totalmente qualificado do arquivo que está sendo registrado. **Win32Error** não é usado e deve ser definido como sem \_ erro. **FailureCode** não é usado e deve ser definido como SPREG \_ Success.

</dd> <dt>

*Param2* 
</dt> <dd>

Se o arquivo estiver sendo registrado, *param2* deverá ser definido como um ponteiro para um valor diferente de zero. Se o registro do arquivo estiver sendo cancelado, *param2* deverá ser definido como um ponteiro para zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Depois de receber a notificação, a função de retorno de chamada pode retornar um dos valores a seguir.



| Código de retorno                                                                                  | Descrição                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anular FILEOP**</dt> </dl> | Não registre ou cancele o registro do arquivo e pare de processar a seção INF.<br/>             |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Registre ou cancele o registro do arquivo e continue processando a seção INF.<br/>                |
| <dl> <dt>**\_ignorar arquivo**</dt> </dl>    | Ignorar registro ou cancelamento de registro do arquivo, mas continuar processando a seção INF<br/> |



 

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

[**SPFILENOTIFY \_ ENDregistro**](spfilenotify-endregistration.md)
</dt> </dl>

 

