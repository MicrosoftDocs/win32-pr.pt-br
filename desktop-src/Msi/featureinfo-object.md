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
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769321"
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
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo é definido como 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




