---
description: A propriedade DVDAdm. DefaultSubpictureLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de subimagem.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriedade DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500733"
---
# <a name="defaultsubpicturelcid-property"></a>Propriedade DefaultSubpictureLCID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm.DefaultSubpictureLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de subimagem.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o LCID da subimagem padrão especificado pelo usuário como armazenado nas configurações do registro para o aplicativo de DVD. Esse valor não é necessariamente o mesmo que o fluxo de subimagem padrão como criado no DVD. Para obter o intervalo de LCIDs válidos, consulte a documentação do Win32 no SDK da plataforma.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação sem valor padrão. Se nenhum LCID de subimagem padrão for especificado, o objeto MSDVDAdm reproduzirá o fluxo de subimagem marcado como o fluxo padrão no disco.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



