---
description: O método SetMediaTimes define as horas de parada e de início da mídia.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Método IAMTimelineSrc:: SetMediaTimes (QEdit. h)'
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
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810223"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Método IAMTimelineSrc:: SetMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaTimes` método define as horas de parada e de início da mídia.

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

Hora de início da mídia, em unidades de 100 a nanossegundos.

</dd> <dt>

*Parar* 
</dt> <dd>

Hora de parada da mídia, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

As horas de mídia são as horas de parada e de início relativas ao arquivo de mídia original. Sempre defina os horários de mídia ao adicionar uma fonte de vídeo ou áudio à linha do tempo. Caso contrário, podem ocorrer problemas de renderização. A hora de parada deve ser maior que a hora de início.

Para usar um quadro ainda de uma fonte de vídeo, defina a hora de parada como um valor fracionário mais do que a hora de início, como 100 nanossegundos. Configurá-los com o mesmo valor causa um erro de renderização.

Se a duração da linha do tempo não corresponder à duração da mídia, a origem será ampliada ou reduzida adequadamente. Isso faz com que o clipe seja reproduzido mais devagar ou mais rápido do que a taxa de criação. (A mudança de densidade ocorrerá em uma fonte de áudio.) Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).

Você pode especificar a duração do arquivo de origem chamando o método [**SetMediaLength**](iamtimelinesrc-setmedialength.md) . Se você definir uma hora de parada de mídia que exceda a duração, o DES truncará a hora de parada.

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

 

 




