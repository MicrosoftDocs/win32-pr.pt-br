---
description: Um objeto SWbemMethodSet é uma coleção de objetos SWbemMethod. Os itens são recuperados usando o método item. Para obter mais informações, consulte Acessando uma coleção. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objeto SWbemMethodSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828661"
---
# <a name="swbemmethodset-object"></a>Objeto SWbemMethodSet

Um objeto **SWbemMethodSet** é uma coleção de objetos [**SWbemMethod**](swbemmethod.md) . Os itens são recuperados usando o método [**Item**](swbemmethodset-item.md) . Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md). Este objeto não pode ser criado pela chamada VBScript **CreateObject** .

> [!Note]  
> Nesta versão da API, não há suporte para o acesso de gravação para informações de método. Se você quiser definir métodos ou modificar definições de método existentes, poderá definir as alterações de método em um arquivo MOF e enviar as alterações usando o compilador MOF. Como alternativa, use a API COM do WMI.

 

## <a name="members"></a>Membros

O objeto **SWbemMethodSet** tem estes tipos de membros:

-   [Métodos](#swbemmethodset-object)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemMethodSet** tem esses métodos.



| Método                              | Descrição                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Item**](swbemmethodset-item.md) | Recupera um objeto [**SWbemMethod**](swbemmethod.md) da coleção. Este é o método de automação padrão deste objeto.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemMethodSet** tem essas propriedades.



| Propriedade                                         | Tipo de acesso          | Descrição                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contar**](swbemmethodset-count.md)<br/> | Somente leitura<br/> | Número de itens na coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHODSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemMethodSet de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




