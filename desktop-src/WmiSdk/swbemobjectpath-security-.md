---
description: A propriedade Security do objeto SWbemObjectPath é usada para obter ou definir os componentes de segurança de um caminho de objeto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_ propriedade (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ed473049de6973da077b1ccfabdd3fe752ff4e5edd13f4a49a7c5589309ae81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639966"
---
# <a name="swbemobjectpathsecurity_-property"></a>Propriedade SWbemObjectPath.Security \_

A **propriedade Security** do objeto [**SWbemObjectPath**](swbemobjectpath.md) é usada para obter ou definir os componentes de segurança de um caminho de objeto. Observe que ele não é usado para definir atributos de segurança do **próprio objeto SWbemObjectPath.** Ele é usado apenas para representar os componentes de segurança do caminho para um [**objeto SWbemLocator.**](swbemlocator.md) Essa propriedade é um [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Definir a [**propriedade \_ Security**](swbemobject-security-.md) de um objeto [**SWbemObjectPath**](swbemobjectset.md) como **NULL** concede acesso ilimitado a todos o tempo todo. Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para obter mais informações, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Definindo a segurança \_ do processo de aplicativo \_ cliente](setting-client-application-process-security.md)
</dt> </dl>

 

 




