---
description: O \_ método Put size define o tamanho de saída e o modo Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: método de ut_Size de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783383"
---
# <a name="iresizeput_size-method"></a>IResize: método de tamanho de UT:p \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Size` método define o tamanho de saída e o modo de ampliação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Altura* \[ no\]
</dt> <dd>

A altura do vídeo, em pixels.

</dd> <dt>

*Largura* \[ no\]
</dt> <dd>

A largura do vídeo, em pixels.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

O modo de ampliação. Consulte [**redimensionar sinalizadores**](resize-flags.md) para obter os valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

O DES pode chamar esse método antes ou depois de chamar **Put \_ MediaType**. Se o DES chamar esse método antes de chamar **Put \_ MediaType**, o filtro deverá selecionar um valor padrão para a profundidade de bits e usar os valores de tamanho para construir um tipo de mídia de saída. Se o DES chamar esse método depois de chamar **Put \_ MediaType**, o filtro deverá modificar seu tipo de saída atual com os novos tamanhos.

O DES também pode chamar esse método depois que o pino de saída estiver conectado. Nesse caso, modifique o tipo de saída e reconecte o pino de saída com o novo tipo. Consulte [reconectando Pins](reconnecting-pins.md) para obter mais informações.

O parâmetro *flags* especifica como o filtro deve executar a operação de redimensionamento.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9,0 ou posterior<br/>                                                         |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




