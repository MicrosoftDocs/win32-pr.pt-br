---
description: Você pode usar as propriedades do objeto SWbemQualifier para representar um único qualificador de uma classe, instância, propriedade ou parâmetro de método WMI. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objeto SWbemQualifier (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165189"
---
# <a name="swbemqualifier-object"></a>Objeto SWbemQualifier

Você pode usar as propriedades do objeto **SWbemQualifier** para representar um único qualificador de uma classe, instância, propriedade ou parâmetro de método WMI. Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membros

O objeto **SWbemQualifier** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SWbemQualifier** tem essas propriedades.



| Propriedade                                                                       | Tipo de acesso           | Descrição                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**Isemendado**](swbemqualifier-isamended.md)<br/>                       | Somente leitura<br/>  | Valor booliano que indica se este qualificador foi localizado usando uma operação de mesclagem.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Somente leitura<br/>  | Valor booliano que indica se esse qualificador é local.<br/>                                   |
| [**IsOverridable**](swbemqualifier-isoverridable.md)<br/>               | Leitura/gravação<br/> | Valor booliano que indica se este qualificador pode ser substituído quando propagado.<br/>          |
| [**Nome**](swbemqualifier-name.md)<br/>                                 | Somente leitura<br/>  | Nome deste qualificador.<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | Leitura/gravação<br/> | Valor booliano que indica se esse qualificador pode ser propagado para uma instância.<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | Somente leitura<br/>  | Valor booliano que indica se esse qualificador pode ser propagado para uma subclasse.<br/>            |
| [**Valor**](swbemqualifier-value.md)<br/>                               | Leitura/gravação<br/> | Valor de variante deste qualificador. Essa é a propriedade padrão deste objeto.<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMQUALIFIER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemQualifier de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




