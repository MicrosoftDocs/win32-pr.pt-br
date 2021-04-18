---
description: O método SetStreamNumber especifica qual fluxo deve ser lido do arquivo de origem associado a esse objeto de origem.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Método IAMTimelineSrc:: SetStreamNumber (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784024"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>Método IAMTimelineSrc:: SetStreamNumber

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetStreamNumber` método especifica qual fluxo deve ser lido do arquivo de origem associado a esse objeto de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* 
</dt> <dd>

O número do fluxo, do conjunto de fluxos que correspondem ao tipo de mídia do grupo pai.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O parâmetro *Val* especifica um número de fluxo do conjunto de fluxos que corresponde ao tipo de mídia do grupo pai, não de todo o conjunto de fluxos no arquivo de origem. Por exemplo, por exemplo, suponha que um arquivo contenha dois fluxos de vídeo e dois fluxos de áudio. Se o objeto de origem estiver dentro de um grupo de vídeos, a definição de *Val* como 0 selecionará o primeiro fluxo de vídeo. O chamador é responsável por especificar um número de fluxo válido.

O número do fluxo assume como padrão zero.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




