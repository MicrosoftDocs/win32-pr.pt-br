---
title: Suporte à localização para controles comuns
description: Este tópico descreve o suporte para idiomas nacionais que são incorporados aos controles comuns.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916065"
---
# <a name="localization-support-for-common-controls"></a>Suporte à localização para controles comuns

Este tópico descreve o suporte para idiomas nacionais que são incorporados aos controles comuns. O suporte ao idioma nacional interno simplifica a implementação de aplicativos localizados.

Este tópico contém as seguintes seções:

-   [Especificando um idioma para os controles comuns](#specifying-a-language-for-the-common-controls)
-   [Especificando um idioma para controles em uma caixa de diálogo](#specifying-a-language-for-controls-in-a-dialog-box)
-   [Tópicos relacionados](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>Especificando um idioma para os controles comuns

Se você quiser especificar um idioma para os controles comuns que seja diferente do idioma do sistema, chame [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). O idioma especificado por essa função se aplica somente ao processo do qual a função é chamada.

Para determinar o idioma que está sendo usado atualmente pelos controles comuns, chame [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage). Ele retorna o valor que foi definido por uma chamada anterior para [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). O idioma retornado é aquele que foi especificado para o processo do qual ele é chamado. Se **InitMUILanguage** não tiver sido chamado ou for chamado de outro processo, **GetMUILanguage** retornará um valor padrão.

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>Especificando um idioma para controles em uma caixa de diálogo

Ao contrário dos controles comuns, os controles predefinidos, como botões ou caixas de edição, não usam o idioma do sistema atual por padrão. O controle de fonte nativo é um controle invisível que funciona em segundo plano para permitir que os controles predefinidos de uma caixa de diálogo exibam o idioma atual do sistema.

Para usar o controle de fonte nativo, siga este procedimento.

1.  Inicialize o controle de fonte nativo chamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Defina o membro **dwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) apontada por *LPINITCTRLS* para a \_ classe NATIVEFNTCTL ICC \_ .
2.  Adicione o controle ao script de recurso para a caixa de diálogo. Defina um ou mais dos seguintes sinalizadores de estilo para especificar quais controles serão afetados. 

    | Sinalizador              | Aplica-se a                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | edição de NFS \_         | Editar controles                                                                                                                                                                                                                                                    |
    | NFS \_ estático       | Controles estáticos                                                                                                                                                                                                                                                  |
    | \_LISTCOMBO NFS    | Controles List, ComboBox, List-View e ComboBoxEx                                                                                                                                                                                                               |
    | \_botão NFS       | Controles de botão                                                                                                                                                                                                                                                  |
    | \_todos os NFS          | Todos os controles                                                                                                                                                                                                                                                     |
    | \_USEFONTASSOC NFS | Plataforma leste asiático. O controle usa o recurso de associação de fonte em vez de alternar para a fonte nativa. Todas as outras plataformas a ignoram. Isso foi preterido para o Windows Vista e não tem suporte no COMCTL v6. Isso existe no COMCTL v5 por motivos herdados. |

    

     

O exemplo a seguir ilustra como adicionar um controle de fonte nativo a um script de recurso. Isso faz com que os controles de edição, lista e combinação da caixa de diálogo exibam texto usando o idioma atual do sistema.


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles comuns](common-controls-intro.md)
</dt> </dl>

 

 




