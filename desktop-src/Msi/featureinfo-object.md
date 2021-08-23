---
description: O objeto FeatureInfo contém informações sobre o recurso de destino e é criado a partir do objeto de sessão usando o método FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objeto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328366"
---
# <a name="featureinfo-object"></a>Objeto FeatureInfo

O objeto **FeatureInfo** contém informações sobre o recurso de destino e é criado a partir do objeto de [**sessão**](session-object.md) usando o método [**FeatureInfo**](session-featureinfo.md) .

## <a name="members"></a>Membros

O objeto **FeatureInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **FeatureInfo** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso           | Descrição                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Atributos**](featureinfo-attributes.md)<br/>   | Leitura/gravação<br/> | Retorna o valor do recurso na coluna atributos da tabela de recursos.<br/> |
| [**Descrição**](featureinfo-description.md)<br/> |                       | Retorna a descrição do recurso.<br/>                                          |
| [**Título**](featureinfo-title.md)<br/>             | Somente leitura<br/>  | Retorna o título do recurso.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo é definido como 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




