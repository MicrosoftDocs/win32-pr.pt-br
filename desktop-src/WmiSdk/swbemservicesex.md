---
description: Estende a funcionalidade do SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objeto SWbemServicesEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091282"
---
# <a name="swbemservicesex-object"></a>Objeto SWbemServicesEx

O objeto **SWbemServicesEx** estende a funcionalidade de [**SWbemServices**](swbemservices.md). Os métodos [**Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) permitem que uma classe ou uma instância seja salva em vários namespaces ou em um namespace diferente daquele em que uma instância foi criada. Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membros

O objeto **SWbemServicesEx** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **SWbemServicesEx** tem esses métodos.



| Método                                       | Descrição                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Posicione**](swbemservicesex-put.md)           | Salva o objeto no namespace associado ao objeto **SWbemServicesEx** e retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que contém o caminho do objeto no qual os dados foram gravados.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Salva um objeto de forma assíncrona em um namespace.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

Os métodos nessa classe podem ser chamados no modo semisynchronous ou no modo assíncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_ISWBEMSERVICESEX CLSID<br/>                                                      |
| IID<br/>                      | ISWbemServicesEx de IID \_<br/>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

