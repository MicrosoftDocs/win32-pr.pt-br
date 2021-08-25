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
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898066"
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
| [**Nome**](swbemproperty-name.md)<br/>                | Somente leitura<br/>  | Nome dessa propriedade WMI.<br/>                                                                                         |
| [**Origem**](swbemproperty-origin.md)<br/>            | Somente leitura<br/>  | Contém a classe de origem desta propriedade.<br/>                                                                   |
| [**Qualificadores\_**](swbemproperty-qualifiers-.md)<br/> | Somente leitura<br/>  | Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) , que é a coleção de qualificadores para essa propriedade.<br/> |
| [**Valor**](swbemproperty-value.md)<br/>              | Leitura/gravação<br/> | Valor real dessa propriedade. Esta é a propriedade de automação padrão deste objeto.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemProperty de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




