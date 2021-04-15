---
description: O valor da propriedade Resumo da entidade transmite o nome do produto, da transformação ou do patch que é instalado pelo pacote.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propriedade de resumo do assunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747319"
---
# <a name="subject-summary-property"></a>Propriedade de resumo do assunto

O valor da propriedade **Resumo da entidade** transmite o nome do produto, da transformação ou do patch que é instalado pelo pacote.

Cabe ao autor de um banco de dados de instalação, transformação ou pacote de patch para fornecer o valor dessa propriedade nas informações de resumo. Os autores devem fazer o seguinte para determinar o valor correto.

-   Defina a propriedade **Resumo do assunto** em um pacote de instalação para o mesmo valor que a propriedade [**ProductName**](productname.md) .
-   Defina a propriedade **Resumo da entidade** em uma transformação para o mesmo valor que a propriedade Resumo do **assunto** no pacote de instalação original.
-   Defina a propriedade **Resumo do assunto** nas informações resumidas de um pacote de patch para uma breve descrição do patch que inclui o nome do produto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




