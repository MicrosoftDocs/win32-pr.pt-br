---
description: O método SetPreviewMode define o modo de visualização para o grupo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: Método IAMTimelineGroup::SetPreviewMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f4c53372066ec28f3782fe53148eaba99489187c3be9b9ccf73195a7b1e6da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756306"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>Método IAMTimelineGroup::SetPreviewMode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método SetPreviewMode define o modo de visualização para o grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fPreview* 
</dt> <dd>

O modo de visualização. Se **TRUE**, o grupo está no modo de visualização. Se **FALSE**, o grupo está no modo de autor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

No modo de visualização, os quadros são descartados durante efeitos lentos ou transições para manter o vídeo sincronizado com o áudio. O vídeo pode parecer muito ruim como resultado. No modo de autor, cada quadro é renderizado. O modo de autor é apropriado para a escrita de arquivos; para a versão prévia na tela, o vídeo pode estar fora de sincronia com o áudio.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineGroup Interface**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




