---
description: O objeto SWbemProperty representa uma única propriedade WMI de um objeto gerenciado. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objeto SWbemProperty (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171970"
---
# <a name="swbemproperty-object"></a>Objeto SWbemProperty

O objeto **SWbemProperty** representa uma única propriedade WMI de um objeto gerenciado. Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membros

O objeto **SWbemProperty** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SWbemProperty** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso           | Descrição                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | Somente leitura<br/>  | Tipo desta propriedade.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Somente leitura<br/>  | Valor booliano que indica se essa propriedade tem um tipo de matriz.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Somente leitura<br/>  | Valor booliano que indica se essa propriedade é local.<br/>                                                            |
| [**Name**](swbemproperty-name.md)<br/>                | Somente leitura<br/>  | Nome dessa propriedade WMI.<br/>                                                                                         |
| [**Ter**](swbemproperty-origin.md)<br/>            | Somente leitura<br/>  | Contém a classe de origem desta propriedade.<br/>                                                                   |
| [**Qualificadores\_**](swbemproperty-qualifiers-.md)<br/> | Somente leitura<br/>  | Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) , que é a coleção de qualificadores para essa propriedade.<br/> |
| [**Valor**](swbemproperty-value.md)<br/>              | Leitura/gravação<br/> | Valor real dessa propriedade. Esta é a propriedade de automação padrão deste objeto.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemProperty de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




