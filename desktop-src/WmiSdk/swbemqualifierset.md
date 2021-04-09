---
description: Um objeto SWbemQualifierSet é uma coleção de objetos SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objeto SWbemQualifierSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011750"
---
# <a name="swbemqualifierset-object"></a>Objeto SWbemQualifierSet

Um objeto **SWbemQualifierSet** é uma coleção de objetos [**SWbemQualifier**](swbemqualifier.md) . Os itens são adicionados à coleção usando o método [**Add**](swbemqualifierset-add.md) , recuperado da coleção usando o método [**Item**](swbemqualifierset-item.md) e removidos da coleção usando o método [**Remove**](swbemqualifierset-remove.md) . Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .

Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

Os objetos [**SWbemQualifier**](swbemqualifier.md) que compõem uma coleção **SWbemQualifierSet** descrevem os qualificadores anexados a uma classe, instância, método ou parâmetro de método de WMI.

## <a name="members"></a>Membros

O objeto **SWbemQualifierSet** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemQualifierSet** tem esses métodos.



| Método                                     | Descrição                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Agrega**](swbemqualifierset-add.md)       | Adiciona um objeto [**SWbemQualifier**](swbemqualifier.md) à coleção **SWbemQualifierSet** .<br/> |
| [**Item**](swbemqualifierset-item.md)     | Retorna um objeto nomeado [**SWbemQualifier**](swbemqualifier.md) da coleção.<br/>             |
| [**Remover**](swbemqualifierset-remove.md) | Exclui um qualificador nomeado da coleção.<br/>                                                   |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemQualifierSet** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Contar**](swbemqualifierset-count.md)<br/> | Somente leitura<br/> | Contém o número de itens em uma coleção **SWbemQualifierSet** .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemQualifierSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




