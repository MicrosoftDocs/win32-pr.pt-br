---
description: A propriedade DVDAdm. DefaultAudioLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propriedade DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780638"
---
# <a name="defaultaudiolcid-property"></a>Propriedade DefaultAudioLCID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm.DefaultAudioLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o LCID de áudio padrão especificado pelo usuário como armazenado nas configurações do registro para o aplicativo de DVD. Esse valor não é necessariamente o mesmo que o fluxo de áudio padrão, como criado no DVD.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação sem valor padrão. Se nenhum LCID de áudio padrão for especificado, o objeto MSDVDAdm reproduzirá o fluxo de áudio marcado como o fluxo padrão no disco.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



