---
description: A propriedade DVDAdm.DefaultSubpictureLCID define ou recupera a configuração do Registro para o LCID padrão especificado pelo usuário para o fluxo de subpicture.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriedade DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc67be112349a050df45f625fda6488c91b22dee357c820724de5842c156894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952985"
---
# <a name="defaultsubpicturelcid-property"></a>Propriedade DefaultSubpictureLCID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A propriedade define ou recupera a configuração do Registro para o LCID padrão especificado pelo `DVDAdm.DefaultSubpictureLCID` usuário para o fluxo de subpicture.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor Inteiro que representa o LCID da subpicture padrão especificado pelo usuário, conforme armazenado nas configurações do Registro para o aplicativo de DVD. Esse valor não é necessariamente o mesmo que o fluxo de subpicture padrão, conforme o autor no DVD. Para o intervalo de LCIDs válidos, consulte a documentação do Win32 no SDK da Plataforma.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação sem valor padrão. Se nenhum LCID de subpicture padrão for especificado, o objeto MSDVDAdm reproduzirá o fluxo de subpicture marcado como o fluxo padrão no disco.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



