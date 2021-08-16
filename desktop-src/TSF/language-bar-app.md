---
title: Barra de idiomas (aplicativos TSF)
description: Um aplicativo não pode adicionar itens à barra de idiomas; somente um serviço de texto pode adicionar itens à barra de idiomas.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- TSF (estrutura de serviços de texto), barra de idiomas
- TSF (estrutura de serviços de texto), barra de idiomas
- Aplicativos habilitados para TSF, barra de idiomas
- barra de idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952104"
---
# <a name="language-bar-tsf-applications"></a>Barra de idiomas (aplicativos TSF)

Um aplicativo não pode adicionar itens à barra de idiomas; somente um serviço de texto pode adicionar itens à barra de idiomas. Um aplicativo pode afetar a aparência de determinados itens na barra de idiomas.

O [compartimento \_ \_ \_ DICTATIONSTAT de fala do compartimento GUID](predefined-compartments.md) é usado para indicar o tipo de entrada de fala que o aplicativo pode aceitar: entrada de texto direto (ditado) e/ou comandos de voz. Por padrão, o ditado está habilitado e o comando de voz está desabilitado. Se o aplicativo puder aceitar comandos de voz, ele deverá definir o valor de [comando do TF \_ \_ habilitado](speech-recognition-constants.md) no \_ compartimento de DICTATIONSTAT de fala do compartimento de GUID \_ \_ . Se o aplicativo puder aceitar o ditado, ele deverá definir o \_ valor habilitado de ditado TF \_ no compartimento GUID \_ DICTATIONSTAT de \_ fala \_ . O \_ ditado TF \_ ou o \_ comando TF \_ no valor desse compartimento determina qual modo (ditado ou comando) a entrada de fala está atualmente em.

Se o aplicativo oferecer suporte ao armazenamento persistente de dados de propriedade, ele deverá definir o compartimento de [ \_ \_ PERSISTMENUENABLED do compartimento de GUID](predefined-compartments.md) como um valor diferente de zero. Isso faz com que o serviço de texto de fala habilite o item de menu **salvar dados de fala** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como configurar a estrutura de serviços de texto](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de idiomas (serviços de texto)](language-bar.md)
</dt> </dl>

 

 




