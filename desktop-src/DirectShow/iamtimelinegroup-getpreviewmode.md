---
description: O método getpreviewmode recupera o modo de visualização para o grupo.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Método IAMTimelineGroup:: getpreviewmode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768793"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a>Método IAMTimelineGroup:: getpreviewmode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetPreviewMode` método recupera o modo de visualização para o grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfPreview* 
</dt> <dd>

Recebe um valor booliano que indica o modo de visualização. Se for **true**, o grupo estará no modo de visualização. Se for **false**, o grupo estará no modo de criação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

No modo de visualização, os quadros são removidos durante efeitos lentos ou transições para manter o vídeo sincronizado com o áudio. O vídeo pode parecer instável como resultado. No modo de criação, cada quadro é renderizado. O modo de criação é apropriado para gravar arquivos; para visualização na tela, o vídeo pode ficar fora de sincronia com o áudio.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




