---
description: Estende o objeto IShellDispatch com uma variedade de novas funcionalidades.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objeto IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 481e64c00ced458be05255af451206a42d449c42d157794dfd1077cf2dda278a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721086"
---
# <a name="ishelldispatch2-object"></a>Objeto IShellDispatch2

Estende o objeto [**IShellDispatch**](ishelldispatch.md) com uma variedade de novas funcionalidades.

> [!Note]  
> **IShellDispatch2** é implementado e acessado por meio do objeto [**shell**](shell.md) .

 

## <a name="members"></a>Membros

O objeto **IShellDispatch2** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **IShellDispatch2** tem esses métodos.



| Método                                                               | Descrição                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Determina se o usuário atual pode iniciar e parar o serviço nomeado.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Exibe a caixa de diálogo **Localizar impressora** .<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Recupera informações do sistema.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Recupera a configuração de restrição de um grupo do registro.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Retorna um valor que indica se um serviço específico está em execução.<br/> |
| [**Iniciar**](ishelldispatch2-servicestart.md)                 | Inicia um serviço nomeado.<br/>                                                 |
| [**Parar**](ishelldispatch2-servicestop.md)                   | Interrompe um serviço nomeado.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Executa uma operação especificada em um arquivo especificado.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Exibe uma barra de navegador.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

para obter uma discussão sobre os serviços de Windows, consulte a documentação de [serviços](../services/services.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
