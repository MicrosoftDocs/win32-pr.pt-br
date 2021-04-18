---
description: O método GetDefaultFPS recupera a taxa de quadros padrão do objeto de origem. O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros a partir da origem original.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Método IAMTimelineSrc:: GetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810394"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>Método IAMTimelineSrc:: GetDefaultFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultFPS` método recupera a taxa de quadros padrão do objeto de origem. O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros a partir da origem original.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFPS* 
</dt> <dd>

Recebe a taxa de quadros padrão, em quadros por segundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A taxa de quadros padrão não será necessária se o formato de arquivo especificar a taxa de quadros. Esse é o caso de formatos de áudio e vídeo.

Se a origem for um bitmap ou uma imagem JPEG, o mecanismo de renderização o usará como a primeira imagem em uma sequência de DIB (bitmap independente de dispositivo), com uma taxa de quadros igual à taxa de quadros padrão. Para renderizar uma imagem estática, em vez de uma sequência DIB, defina a taxa de quadros padrão como 0.

Se a origem for um GIF, não defina a taxa de quadros. Para GIFs animados, o arquivo GIF especifica o atraso entre cada imagem.

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

 

 




