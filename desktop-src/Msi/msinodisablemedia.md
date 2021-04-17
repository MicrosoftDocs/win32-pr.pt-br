---
description: Defina a propriedade MSINODISABLEMEDIA para impedir que o instalador defina a propriedade DISABLEMEDIA. Definir a propriedade DISABLEMEDIA impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propriedade MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748765"
---
# <a name="msinodisablemedia-property"></a>Propriedade MSINODISABLEMEDIA

Defina a propriedade **MSINODISABLEMEDIA** para impedir que o instalador defina a propriedade [**DISABLEMEDIA**](-disablemedia.md) . Definir a propriedade **DISABLEMEDIA** impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.

Quando **MSINODISABLEMEDIA** não estiver definido, o instalador poderá adicionar [**DISABLEMEDIA**](-disablemedia.md) ao fluxo de propriedade administrativa ao executar uma [instalação administrativa](administrative-installation.md). Isso impede que os usuários que instalam a partir da imagem administrativa nunca instalem a partir da mídia, como um CD-ROM.

-   Ao executar uma instalação administrativa, o instalador só adicionará [**DISABLEMEDIA**](-disablemedia.md) ao fluxo de propriedade administrativa se a propriedade de [**Resumo contagem de páginas**](page-count-summary.md) for menor que 150.

Se [**DISABLEMEDIA**](-disablemedia.md) estiver listado na propriedade [**adminproperties**](adminproperties.md) , definir **MSINODISABLEMEDIA** impedirá que **DISABLEMEDIA** seja definido durante uma instalação administrativa. Nesse caso, o instalador pode registrar uma fonte de mídia e um usuário pode ter a opção de reinstalar a partir da origem de mídia se a imagem de instalação administrativa original ficou indisponível posteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003, Windows XP e Windows 2000. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




