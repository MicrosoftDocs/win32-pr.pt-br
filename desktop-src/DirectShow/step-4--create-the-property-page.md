---
description: Etapa 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Etapa 4. Criar a página de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172351"
---
# <a name="step-4-create-the-property-page"></a>Etapa 4. Criar a página de propriedades

Neste ponto, o filtro dá suporte a tudo o que precisa para uma página de propriedades. A próxima etapa é implementar a própria página de propriedades. Comece derivando uma nova classe de **CBasePropertyPage**. O exemplo a seguir mostra parte da declaração, incluindo algumas variáveis de membro privado que serão usadas posteriormente no exemplo:


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



Em seguida, crie um recurso de caixa de diálogo no editor de recursos, junto com um recurso de cadeia de caracteres para o título da caixa de diálogo. A cadeia de caracteres aparecerá na guia da página de propriedades. As duas IDs de recurso são argumentos para o construtor **CBasePropertyPage** :


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



A ilustração a seguir mostra o recurso de caixa de diálogo para a página de propriedades de exemplo.

![caixa de diálogo página de propriedades](images/proppage.png)

Agora você está pronto para implementar a página de propriedades. Estes são os métodos em **CBasePropertyPage** para substituir:

-   **OnConnect** é chamado quando o cliente cria a página de propriedades. Ele define o ponteiro **IUnknown** para o filtro.
-   **OnActivate** é chamado quando a caixa de diálogo é criada.
-   **OnReceiveMessage** é chamado quando a caixa de diálogo recebe uma mensagem de janela.
-   **OnApplyChanges** é chamado quando o usuário confirma as alterações de propriedade clicando no botão **OK** ou **aplicar** .
-   **OnDisconnect** é chamado quando o usuário ignora a folha de propriedades.

O restante deste tutorial descreve cada um desses métodos.

Em seguida: [etapa 5. Armazene um ponteiro para o filtro](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



