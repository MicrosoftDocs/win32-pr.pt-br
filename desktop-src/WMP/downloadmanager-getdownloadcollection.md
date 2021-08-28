---
title: Método DownloadManager.getDownloadCollection
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método getDownloadCollection recupera a coleção de download especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Método getDownloadCollection Windows Media Player
- Método getDownloadCollection Windows Media Player , classe DownloadManager
- Classe DownloadManager Windows Media Player , método getDownloadCollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57fc729296f15b39e603683cab38e3d0d878733ab0990d9876e32b4001a15cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749616"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>Método DownloadManager.getDownloadCollection

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **método getDownloadCollection** recupera a coleção de download especificada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*collectionId* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando a ID da coleção de download a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto DownloadCollection.**

## <a name="remarks"></a>Comentários

Primeiro, você deve chamar *DownloadManager.* **createDownloadCollection** para criar uma nova coleção e recuperar seu valor de ID.

Uma coleção de download existente pode conter itens que foram marcados como cancelados.

Itens de download em tempo real não concluídos em uma sessão anterior não são recuperados como parte da coleção. Os downloads em segundo plano que foram concluídos antes da sessão atual permanecem na coleção de download até a remoção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





