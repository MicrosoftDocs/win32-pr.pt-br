---
title: Método GetIndexMode IConfigAsfWriter
description: O método GetIndexMode recupera o modo de índice temporal atual.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Formato de mídia do windows do método GetIndexMode
- Método GetIndexMode windows Formato de Mídia, interface IConfigAsfWriter
- Formato de mídia da interface IConfigAsfWriter , método GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95eb0e037bbebf62b710317b6e4b9b1224f9d2429712ffaec88dd1703a1c667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655457"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Método IConfigAsfWriter::GetIndexMode

O **método GetIndexMode** recupera o modo de índice temporal atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbIndexFile* \[ out\]
</dt> <dd>

Ponteiro para uma variável do tipo **BOOL** que recebe a configuração de modo de índice temporal. Um valor **TRUE** indica que o Wm ASF Writer está configurado para gravar arquivos indexados temporalmente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="remarks"></a>Comentários

Use esse método para determinar se o [Wm ASF Writer](wm-asf-writer-filter.md) está configurado atualmente para gravar arquivos ASF indexados temporalmente. Para obter mais informações sobre arquivos indexados temporalmente e indexados por quadro, consulte Os Comentários de [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 