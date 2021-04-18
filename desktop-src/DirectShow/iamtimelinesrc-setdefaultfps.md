---
description: O método SetDefaultFPS define a taxa de quadros padrão do objeto de origem.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Método IAMTimelineSrc:: SetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758679"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>Método IAMTimelineSrc:: SetDefaultFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDefaultFPS` método define a taxa de quadros padrão do objeto de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QUADROS* 
</dt> <dd>

Taxa de quadros padrão, em quadros por segundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido, ou E \_ INVALIDARG se a taxa de quadros especificada for menor que zero.

## <a name="remarks"></a>Comentários

O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros do arquivo de origem original.

Chame esse método somente para arquivos de origem sem uma taxa de quadros predefinida. Para arquivos bitmap e JPEG, a taxa de quadros padrão é zero, o que faz com que a origem seja renderizada como uma imagem ainda. Para usar a imagem, como o primeiro quadro em uma sequência DIB, defina a taxa de quadros como um valor maior que zero. Para obter mais informações, consulte [trabalhando com fontes](working-with-sources.md).

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

 

 




