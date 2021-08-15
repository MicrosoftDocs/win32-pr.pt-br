---
description: O método IsSubpictureStreamEnabled recupera um valor que indica se o fluxo de subpicture especificado está habilitado no título atual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc982120b6a7a57d59d5213fc57b5ba3851d7d9d2f4c3e553fba97d3307d8bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817043"
---
# <a name="issubpicturestreamenabled-method"></a>Método IsSubpictureStreamEnabled

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `IsSubpictureStreamEnabled` método recupera um valor que indica se o fluxo de subpicture especificado está habilitado no título atual.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica o fluxo de subspícone como um Inteiro.



| Valor   | Descrição              |
|---------|--------------------------|
| 0 a 31 | fluxo de subpicture        |
| 63      | fluxo de taxa de bits baixa em mute |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliana que indica se o fluxo de áudio especificado está disponível no título atual. True significa que ele está disponível.

## <a name="remarks"></a>Comentários

Embora um disco possa conter até 32 fluxos de subpicture, cada fluxo não está necessariamente disponível para cada título. Sempre verifique se um fluxo está disponível para um título antes de definir a [**propriedade CurrentSubpictureStream.**](currentsubpicturestream-property.md)

 

 



