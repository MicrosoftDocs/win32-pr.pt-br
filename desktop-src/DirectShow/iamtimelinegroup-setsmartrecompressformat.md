---
description: O método SetSmartRecompressFormat especifica um formato de compactação de vídeo a ser usado para a recompactação inteligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'Método IAMTimelineGroup:: SetSmartRecompressFormat (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810400"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>Método IAMTimelineGroup:: SetSmartRecompressFormat

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetSmartRecompressFormat` método especifica um formato de compactação de vídeo a ser usado para a recompactação inteligente.

A recompactação inteligente não tem suporte para grupos de áudio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Ponteiro para uma estrutura que descreve o formato de compactação. Atualmente, apenas a estrutura [**SCompFmt0**](scompfmt0.md) é válida. Você deve converter esse parâmetro para um ponteiro do tipo **Long**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) no mesmo grupo, para especificar um formato descompactado.

Se o `SetSmartRecompressFormat` método tiver sucesso, você poderá usar o mecanismo de processamento inteligente para gerar um fluxo de vídeo compactado. O vídeo compactado terá a largura, a altura e a taxa de quadros que foi especificada no parâmetro *pFormat* . Esses valores substituirão aqueles fornecidos para o formato descompactado no método **SetMediaType** . No entanto, para obter os benefícios da recompactação inteligente, os dois formatos devem corresponder. Em outras palavras, os formatos compactados e descompactados devem ter a mesma altura, largura e taxa de quadros.

Se o mecanismo de processamento inteligente não puder produzir o formato compactado, ele produzirá um fluxo de vídeo não compactado. Se isso ocorrer, o mecanismo de processamento inteligente relata que as IDs do DEX não \_ \_ \_ encontrarão \_ erro de renderização de compressor durante o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . O aplicativo pode capturar esse erro por meio do método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . (Para obter mais informações, consulte [registrando](logging-errors.md) erros e [erros de renderização](rendering-errors.md).)

O formato de recompactação inteligente não é persistente. Se um aplicativo usar a recompactação inteligente, ele deverá definir o formato de recompactação sempre que carregar um arquivo de projeto.

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
</dt> <dt>

[Mecanismo de processamento inteligente](smart-render-engine.md)
</dt> <dt>

[Gravando um projeto em um arquivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




