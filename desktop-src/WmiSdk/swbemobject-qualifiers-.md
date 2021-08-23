---
description: A propriedade Qualifiers \_ do objeto SWbemObject retorna um objeto SWbemQualifierSet que é uma coleção de qualificadores para a classe ou instância atual. Esta propriedade é somente para leitura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732486"
---
# <a name="swbemobjectqualifiers_-property"></a>Propriedade SWbemObject. Qualifiers \_

A propriedade **Qualifiers \_** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que é uma coleção de qualificadores para a classe ou instância atual. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

A [lista todos os qualificadores para um](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) exemplo de código VBScript da classe WMI na galeria do TechNet usa a \_ Propriedade Qualifier para listar os qualificadores de classe para uma classe WMI especificada.

A amostra de código [listar todas as classes abstratas no WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript na galeria do TechNet lista todas as classes abstratas WMI definidas no \\ namespace raiz cimv2.

A amostra de código [listar todas as classes dinâmicas no WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript usa a \_ Propriedade Qualifier para listar todas as classes dinâmicas WMI (incluindo classes de associação) definidas no \\ namespace raiz cimv2.

O exemplo de código do [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell na galeria do TechNet lista todas as propriedades graváveis no namespace especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 




