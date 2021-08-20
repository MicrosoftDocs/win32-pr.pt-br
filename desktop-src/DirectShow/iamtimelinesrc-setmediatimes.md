---
description: O método SetMediaTimes define os horários de parada e início da mídia.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: Método IAMTimelineSrc::SetMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5de058e31da605b96f7b013c03e9c0d020daa11ec676618b4a13f5ff92e701f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154918"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Método IAMTimelineSrc::SetMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaTimes` método define as horas de início e de parada de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de início da mídia, em unidades de 100 nanossegundos.

</dd> <dt>

*Parar* 
</dt> <dd>

Tempo de parada de mídia, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os tempos de mídia são os horários de parada e início relativos ao arquivo de mídia original. Sempre de acordo com os horários de mídia quando você adiciona uma fonte de áudio ou vídeo à linha do tempo. Caso contrário, poderão ocorrer problemas de renderização. A hora de parada deve ser maior que a hora de início.

Para usar um quadro ainda de uma fonte de vídeo, de definido o tempo de parada como uma quantidade fracionada maior do que a hora de início, como 100 nanossegundos. Defini-los para o mesmo valor causa um erro de renderização.

Se a duração da linha do tempo não corresponder à duração da mídia, a origem se alonga ou reduz de acordo. Isso faz com que o clipe seja reproduzido mais lentamente ou mais rápido do que a taxa de autor. (A mudança de tom ocorrerá em uma fonte de áudio.) Para obter mais informações, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Você pode especificar a duração do arquivo de origem chamando o [**método SetMediaLength.**](iamtimelinesrc-setmedialength.md) Se você definir um tempo de parada de mídia que exceda a duração, o DES truncará a hora de parada.

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

 

 




