---
title: Método DownloadManager. getbaixecollection
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método getdownloadscollection recupera a coleção de download especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- método getbaixecollection Windows Media Player
- método getbaixecollection Windows Media Player, classe DownloadManager
- Classe DownloadManager Windows Media Player, método getbaixecollection
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
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761467"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>Método DownloadManager. getbaixecollection

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **Getdownloadscollection** recupera a coleção de download especificada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CollectionId* \[ no\]
</dt> <dd>

**Número** (**longo**) especificando a ID da coleção de download a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **downloadcollection** .

## <a name="remarks"></a>Comentários

Você deve primeiro chamar *DownloadManager*. **Createbaixecollection** para criar uma nova coleção e recuperar seu valor de ID.

Uma coleção de download existente pode conter itens que foram marcados como cancelados.

Itens de download em tempo real não concluídos em uma sessão anterior não são recuperados como parte da coleção. Os downloads em segundo plano que foram concluídos antes da sessão atual permanecem na coleção de download até serem removidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createbaixecollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Objeto downloadcollection**](downloadcollection-object.md)
</dt> </dl>

 

 





