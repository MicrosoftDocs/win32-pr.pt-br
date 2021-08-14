---
description: O método FixMediaTimes2 fecha os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Esse método é equivalente a IAMTimelineSrc::FixMediaTimes, mas aceita valores REFTIME.
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: Método IAMTimelineSrc::FixMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ceff01e17d82ed59e8d63811841e58e97323a9be4ec4c40b719bb655aac464e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399616"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>Método IAMTimelineSrc::FixMediaTimes2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método faz a rodada dos valores de tempo especificados para o limite de quadro mais `FixMediaTimes2` próximo, conforme definido pela taxa de quadros de saída. Esse método é equivalente a [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em segundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em segundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

 

 




