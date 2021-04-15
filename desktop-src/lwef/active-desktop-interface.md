---
title: Usando o objeto Active Desktop
description: Este artigo contém informações sobre o objeto ActiveDesktop que faz parte da API do shell do Windows. Esse objeto, por meio de sua interface IActiveDesktop, permite que você adicione, remova e altere itens na área de trabalho.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objeto ActiveDesktop
- Área de trabalho ativa
- Enumeração, itens da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453987"
---
# <a name="using-the-active-desktop-object"></a>Usando o objeto Active Desktop

\[Esse recurso tem suporte apenas no Windows XP ou anterior. \]

Este artigo contém informações sobre o objeto **ActiveDesktop** que faz parte da API do shell do Windows. Esse objeto, por meio de sua interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , permite que você adicione, remova e altere itens na área de trabalho.

## <a name="overview-of-the-active-desktop-interface"></a>Visão geral da interface de área de trabalho ativa

-   [Acessando o Active Desktop](#accessing-the-active-desktop)
-   [Adicionando um item da área de trabalho](#adding-a-desktop-item)
-   [Enumerando os itens da área de trabalho](#enumerating-the-desktop-items)

O Active Desktop é um recurso introduzido com o Microsoft Internet Explorer 4,0 que permite incluir documentos e itens HTML (como controles ActiveX da Microsoft e miniaplicativos Java) diretamente em sua área de trabalho. A interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , que faz parte da API do shell do Windows, é usada para adicionar, remover e modificar programaticamente os itens na área de trabalho. Itens de área de trabalho ativas também podem ser adicionados usando um arquivo de formato de definição de canal (CDF).

### <a name="accessing-the-active-desktop"></a>Acessando o Active Desktop

Para acessar o Active Desktop, um aplicativo cliente precisaria criar uma instância do objeto ActiveDesktop (CLSID \_ ActiveDesktop) com a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e recuperar um ponteiro para a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) do objeto.

O exemplo a seguir mostra como recuperar um ponteiro para a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Adicionando um item da área de trabalho

Há três métodos que você pode usar para adicionar um item da área de trabalho: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Cada item da área de trabalho adicionado ao Active Desktop deve ter uma URL de origem diferente.

Os métodos [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) fornecem a opção para exibir as várias interfaces de usuário que podem ser exibidas antes de adicionar um item da área de trabalho ao Active Desktop. As interfaces verificam se os usuários desejam adicionar o item da área de trabalho ao seu Active Desktop. As interfaces também notificam os usuários sobre os riscos de segurança que são garantidos pelas configurações da zona de segurança de URL e perguntarão aos usuários se eles gostariam de criar uma assinatura para esse item da área de trabalho. Os dois métodos também fornecem uma maneira de suprimir as interfaces do usuário. O método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requer uma chamada para [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para atualizar o registro. Para o **IActiveDesktop:: AddDesktopItemWithUI**, o aplicativo cliente deve liberar imediatamente a interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) e, em seguida, usar a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar uma interface para uma instância do objeto **ActiveDesktop** que inclui o item da área de trabalho recém-adicionado.

O método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) adiciona o item da área de trabalho especificado ao Active Desktop sem nenhuma interface do usuário, a menos que as configurações da zona de segurança de URL o impeçam. Se as configurações da zona de segurança da URL não permitirem que o item da área de trabalho seja adicionado sem avisar o usuário, o método falhará. **IActiveDesktop:: AddDesktopItem** também requer uma chamada para [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) a fim de atualizar o registro.

O exemplo a seguir demonstra como adicionar um item da área de trabalho com o método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Enumerando os itens da área de trabalho

Para enumerar os itens da área de trabalho instalados atualmente no Active Desktop, o aplicativo cliente precisa recuperar o número total de itens da área de trabalho instalados usando o método [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) e, em seguida, criando um loop que recupera a estrutura de [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) para cada item da área de trabalho chamando o método [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) usando o índice de item da área de trabalho.

O exemplo a seguir demonstra uma maneira de enumerar os itens da área de trabalho.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 