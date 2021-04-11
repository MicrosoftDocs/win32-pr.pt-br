---
description: A propriedade DVDAdm. DefaultMenuLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriedade DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087824"
---
# <a name="defaultmenulcid-property"></a>Propriedade DefaultMenuLCID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



