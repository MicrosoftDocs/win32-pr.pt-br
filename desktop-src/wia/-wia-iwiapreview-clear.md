---
description: 'Libera a imagem não filtrada armazenada em cache pelo método IWiaPreview:: GetNewPreview. Ele também libera o filtro de processamento de imagem.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Método IWiaPreview:: Clear (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813622"
---
# <a name="iwiapreviewclear-method"></a>Método IWiaPreview:: Clear

Libera a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Ele também libera o filtro de processamento de imagem.

## <a name="syntax"></a>Sintaxe


```C++
void Clear();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Em **IWiaPreview:: limpar** o componente de versão prévia do WIA (Windows Image Acquisition) 2,0 libera todos os ponteiros de interface que ele armazena. O componente de visualização do WIA 2,0 mantém referências a *pWiaItem2* e *PWiaTransferCallback* passados em [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Para ser preciso, o componente de visualização do WIA 2,0 mantém uma referência ao *pWiaItem2* e ao filtro de processamento de imagem do driver, que, por sua vez, mantém uma referência ao *pWiaTransferCallback*. Em **IWiaPreview:: Clear**, o componente de visualização do WIA 2,0 também libera sua referência para *pWiaItem2* e para o filtro de processamento de imagem que, por sua vez, libera sua referência para *pWiaTransferCallback*. O componente de visualização do WIA 2,0 exclui a imagem armazenada em cache e não filtrada internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




