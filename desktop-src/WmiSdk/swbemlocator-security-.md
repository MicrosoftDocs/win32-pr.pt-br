---
description: A \_ Propriedade Security do objeto SWbemLocator é usada para ler ou definir as configurações de segurança para um objeto SWbemLocator. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Propriedade SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661763"
---
# <a name="swbemlocatorsecurity_-property"></a>Propriedade SWbemLocator. Security \_

A **propriedade \_ Security** do objeto [**SWbemLocator**](swbemlocator.md) é usada para ler ou definir as configurações de segurança para um objeto **SWbemLocator** . Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Definir a **propriedade \_ Security** de um objeto [**SWbemLocator**](swbemlocator.md) como **NULL** concede acesso ilimitado a todos os momentos. Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

As propriedades de um objeto **SWbemLocator. \_ Security** não têm valores padrão. Se você tentar obter o valor de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) em um objeto [**SWbemLocator**](swbemlocator.md) antes de defini-lo, ocorrerá um erro de [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | ISWbemLocator de IID \_<br/>                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Definindo a \_ segurança do processo do aplicativo cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**Objeto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




