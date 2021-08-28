---
description: O valor da propriedade Resumo da Assunto transmite o nome do produto, transformação ou patch instalado pelo pacote.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propriedade Resumo da Assunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9d92328f142e4fd47567e92d4fe3bb7f016b0bf058b2932f7e1136687507e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627226"
---
# <a name="subject-summary-property"></a>Propriedade Resumo da Assunto

O valor da propriedade **Resumo da** Assunto transmite o nome do produto, transformação ou patch instalado pelo pacote.

É responsabilidade do autor de um pacote de banco de dados de instalação, transformação ou patch fornecer o valor dessa propriedade nas informações resumidas. Os autores devem fazer o seguinte para determinar o valor correto.

-   De definir **a propriedade Resumo** da Assunto em um pacote de instalação com o mesmo valor que a propriedade [**ProductName.**](productname.md)
-   De definir **a propriedade Resumo da** Assunto em uma transformação com o mesmo valor que a propriedade Resumo **da** Assunto no pacote de instalação original.
-   Descrição **da propriedade Resumo** da Assunto nas informações resumidas de um pacote de patch para uma breve descrição do patch que inclui o nome do produto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descrições da propriedade Summary](summary-property-descriptions.md)
</dt> </dl>

 

 




