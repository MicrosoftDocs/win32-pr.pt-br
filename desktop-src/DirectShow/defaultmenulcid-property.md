---
description: A propriedade DVDAdm. DefaultMenuLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriedade DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906886"
---
# <a name="defaultmenulcid-property"></a>Propriedade DefaultMenuLCID

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDAdm.DefaultMenuLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o LCID como armazenado nas configurações do registro para o aplicativo de DVD. Esse valor não é necessariamente o mesmo que o idioma do menu padrão, conforme criado no DVD. Para obter o intervalo de LCIDs válidos, consulte a documentação do Win32 no SDK da plataforma.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação sem valor padrão. Se nenhum LCID de menu padrão for especificado, o objeto MSDVDAdm usará o idioma marcado como o idioma de menu padrão no disco.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



