---
description: O método FixMediaTimes fecha os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Em geral, os aplicativos não precisam chamar esse método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: Método IAMTimelineSrc::FixMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dcace4e501a27b1f82b148533f382f5c86bafb17d9bf34343f1e43a8893672c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052396"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>Método IAMTimelineSrc::FixMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método faz a rodada dos valores de tempo especificados para o limite de quadro mais `FixMediaTimes` próximo, conforme definido pela taxa de quadros de saída. Em geral, os aplicativos não precisam chamar esse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em unidades de 100 nanossegundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em unidades de 100 nanossegundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é semelhante ao método [**IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md) mas preserva a taxa original de tempos de mídia e tempos de linha do tempo. Apenas arredondando os horários para o limite de quadro mais próximo pode distorcer essa taxa.

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

[**IAMTimelineSrc Interface**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




