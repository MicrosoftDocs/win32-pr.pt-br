---
title: Design de Server-Side
description: As funções do lado do servidor se comunicam com o assistente do cliente por meio do objeto Windows. external. O script do lado do servidor fornece essas funções para responder a eventos do assistente e para recuperar informações sobre o assistente.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- assistentes de publicação, design do lado do servidor
- janela. external, assistentes de publicação
- assistentes de publicação, janela. externa
- assistentes de publicação, funções de script de navegação
- scripts, assistentes de publicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075e5a18b2150e504b6424fae2591ed83fdf707a6a20231b8f1186ddb6f3a67b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555806"
---
# <a name="server-side-design"></a>Design de Server-Side

As funções do lado do servidor se comunicam com o assistente do cliente por meio do objeto **Windows. external** . O script do lado do servidor fornece essas funções para responder a eventos do assistente e para recuperar informações sobre o assistente.

Os tópicos a seguir são abordados neste documento.

-   [Implementando funções de script de navegação](#implementing-navigation-script-functions)
    -   [Voltar ()](#onback)
    -   [OnNext ()](#onnext)
    -   [OnCancel ()](#oncancel)
-   [Outros métodos e propriedades](#other-methods-and-properties)
    -   [Métodos](#methods)
    -   [Propriedades](#properties)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementando funções de script de navegação

O script do lado do servidor em cada página HTML responde aos botões de navegação por meio de funções para **onvoltar**, **OnNext** e **OnCancel**. Essas funções devem ser acessíveis por meio de **IHTMLDocument:: get \_ script** no cliente e não têm parâmetros.

### <a name="onback"></a>Voltar ()

-   Responde quando o usuário clica no botão de **volta** no assistente.
-   Se a página atual do servidor for a primeira página do lado do servidor, chame **Window. external. FinalBack** para instruir o cliente a navegar até a página anterior do lado do cliente.
-   Se a página atual do servidor não for a primeira página do lado do servidor, navegue até a página anterior do lado do servidor.
-   Essa função deve ser implementada para cada página. Qualquer página que não faça isso é considerada inválida e exibe uma página de erro.

### <a name="onnext"></a>OnNext ()

-   Responde quando o usuário clica em **Avançar** no assistente.
-   Se a página atual do servidor for a última página do lado do servidor, chame **Window. external. FinalNext** para instruir o cliente a navegar até a próxima página do lado do cliente ou para concluir o assistente.
-   Se a página atual do servidor não for a última página do lado do servidor, navegue até a próxima página do lado do servidor.

### <a name="oncancel"></a>OnCancel ()

-   Responde quando o usuário clica em **Cancelar** no assistente.
-   A interface de usuário deve ser projetada para que o usuário possa cancelar a qualquer momento.
-   Depois que qualquer processamento na função **OnCancel** for processado, o cliente fechará o assistente.

## <a name="other-methods-and-properties"></a>Outros métodos e propriedades

As funções implementadas pelo cliente são acessadas por meio do **Windows. external**, assim como propriedades. Os serviços disponíveis são os seguintes:

### <a name="methods"></a>Métodos

-   [**Setheadertext**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Propriedades

-   [**Legenda**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propriedade**](/windows/desktop/shell/iwebwizardhost-property)

O exemplo de código a seguir mostra o código do lado do servidor para uma página de assistente simples que implementa a página de erro do serviço Web.


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Design do lado do cliente](pubwiz-client.md)
</dt> <dt>

[Registrando um serviço](pubwiz-reg.md)
</dt> </dl>

 

 