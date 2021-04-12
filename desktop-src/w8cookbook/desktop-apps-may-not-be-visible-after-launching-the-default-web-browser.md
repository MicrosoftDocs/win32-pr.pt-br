---
title: Os aplicativos da área de trabalho podem não estar visíveis depois de iniciar o navegador da Web padrão ou aplicativos da Windows Store
description: Os aplicativos da área de trabalho podem não estar visíveis depois de iniciar o navegador da Web padrão ou aplicativos da Windows Store
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104294542"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>Os aplicativos da área de trabalho podem não estar visíveis depois de iniciar o navegador da Web padrão ou aplicativos da Windows Store

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

A experiência do usuário do aplicativo da Windows Store concentra-se em um único aplicativo de cada vez, com multitarefas, troca de aplicativos e notificações fornecidas pela interface do usuário do Windows. Os aplicativos da Windows Store são dimensionados para preencher o espaço disponível na tela, com a exibição mais comum sendo a tela inteira. Portanto, quando outro aplicativo no sistema é iniciado, você não pode mais supor que o novo aplicativo será aberto em uma janela da área de trabalho junto com seu aplicativo de desktop. Isso é sempre verdadeiro para aplicativos da Windows Store e navegadores que optam por participar da nova experiência de interface do usuário do Windows. Você pode continuar a ver outros aplicativos ao mesmo tempo, por exemplo, se você estiver na área de trabalho e iniciar outro aplicativo de área de trabalho ou se tiver aplicativos em um estado encaixado.

## <a name="manifestation"></a>Manifestação

Quando um aplicativo de área de trabalho usa técnicas comuns de ativação de aplicativo, como usar a API ShellExecute em um arquivo ou protocolo, o Windows inicia o aplicativo associado a esse registro, que pode ser um aplicativo da Windows Store e/ou o navegador da Web padrão do usuário (o navegador da Web padrão pode optar por participar da área de trabalho ou da nova interface de usuário do Windows). Os aplicativos da Windows Store são iniciados usando a tela inteira, ocultando a área de trabalho e o aplicativo de desktop do qual ele foi iniciado.

> [!Note]  
> No Windows 8, o Internet Explorer 10 é configurado como o navegador padrão do usuário, mas o usuário pode optar por instalar e definir outro navegador como o padrão (sem alteração do Windows 7). No Internet Explorer 10, quando um link é aberto de um aplicativo de área de trabalho, o Internet Explorer será aberto na área de trabalho. Mas essa configuração pode ser alterada pelos usuários para que o Internet Explorer seja aberto como um aplicativo da Windows Store. Os fornecedores de navegadores foram incentivados a adotar uma experiência semelhante de "inicialização contextual"; no entanto, os desenvolvedores devem planejar o fato de que nem todos os navegadores se comportarão da mesma forma.

 

## <a name="mitigation"></a>Atenuação

Embora não haja nenhuma alteração que os desenvolvedores possam fazer em seus aplicativos para atenuar esse comportamento, há algo que o usuário final pode fazer para que você se comunique com eles. Considere o uso das informações coletadas pela API ShellExecuteEx estendida () para preencher uma caixa de diálogo apropriadamente adequada. Nessa caixa de diálogo, indique ao usuário qual aplicativo será iniciado e se o aplicativo é um aplicativo da Windows Store ou um aplicativo de área de trabalho. O CLSID pode ser usado para distinguir aplicativos da Windows Store de aplicativos da área de trabalho. Opções de usuário:

-   Os usuários que têm um monitor de tela larga podem ajustar o aplicativo da Windows Store à borda da tela para expor a área de trabalho e, portanto, exibir o aplicativo da Windows Store e o aplicativo de desktop ao mesmo tempo.
-   Se o Internet Explorer estiver configurado como o navegador padrão do usuário, os usuários poderão alterar seu comportamento alterando as opções da Internet no painel de controle. Na guia programas, os usuários podem alterar o modo como o Internet Explorer lida com links. Outros navegadores podem oferecer uma configuração semelhante.

 

 




