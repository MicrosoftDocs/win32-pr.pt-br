---
description: A seção obtendo uma pasta ID abordou duas abordagens para obter um ponteiro do objeto de namespace para uma lista de identificadores de item (PIDL).
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Obtendo informações sobre o conteúdo de uma pasta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988734"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Obtendo informações sobre o conteúdo de uma pasta

A seção [obtendo uma pasta ID](folder-id.md) abordou duas abordagens para obter um ponteiro do objeto de namespace para uma lista de identificadores de item (PIDL). Uma pergunta óbvia é: quando você tem um PIDL, o que pode fazer com ele? Uma pergunta relacionada é: e se nenhuma das abordagens funcionar ou for adequada para seu aplicativo? A resposta a ambas as perguntas requer uma análise mais detalhada de como o namespace é implementado. A chave é a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

-   [Usando a interface IShellFolder](#using-the-ishellfolder-interface)
-   [Enumerando o conteúdo de uma pasta](#enumerating-the-contents-of-a-folder)
-   [Determinando nomes de exibição e outras propriedades](#determining-display-names-and-other-properties)
-   [Obtendo um ponteiro para a interface IShellFolder de uma subpasta](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Determinando a pasta pai de um objeto](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Usando a interface IShellFolder

Anteriormente nesta documentação, as pastas de namespace eram conhecidas como objetos. Embora, nesse ponto, o termo tenha sido usado em um sentido flexível, ele também é realmente verdadeiro em um sentido estrito. Cada pasta de namespace é representada por um objeto de Component Object Model (COM). Cada objeto de pasta expõe várias interfaces que podem ser usadas para uma ampla variedade de tarefas. Algumas interfaces que são opcionais podem não ser expostas por todas as pastas. No entanto, todas as pastas devem expor a interface fundamental, [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).

A primeira etapa no uso de um objeto Folder é recuperar um ponteiro para sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Além de fornecer acesso às outras interfaces do objeto, o **IShellFolder** expõe um grupo de métodos que manipulam várias tarefas comuns, várias das quais são discutidas nesta seção.

Para recuperar um ponteiro para a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de um objeto de namespace, você deve primeiro chamar [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder). Essa função retorna um ponteiro para a interface **IShellFolder** da raiz do namespace, a área de trabalho. Depois de ter a interface **IShellFolder** da área de trabalho, há várias maneiras de continuar.

Se você já tiver o PIDL da pasta em que está interessado — por exemplo, chamando [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)– você pode recuperar sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) chamando o método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) da área de trabalho. Se você tiver o caminho de um objeto do sistema de arquivos, deverá primeiro obter seu PIDL chamando o método IShellFolder da área de trabalho [**::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) e, em seguida, chamar **IShellFolder:: BindToObject**. Se nenhuma dessas abordagens for aplicável, você poderá usar outros métodos **IShellFolder** para navegar no namespace. Para obter mais informações, consulte [navegando no namespace](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Enumerando o conteúdo de uma pasta

A primeira coisa que você geralmente quer fazer com uma pasta é descobrir o que ela contém. Primeiro, você deve chamar o método [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) da pasta. A pasta criará um objeto de enumeração OLE padrão e retornará sua interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) . Essa interface expõe quatro métodos padrão —[**clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)e [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)— que podem ser usados para enumerar o conteúdo da pasta.

O procedimento básico para enumerar o conteúdo de uma pasta é:

1.  Chame o método Folders [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) para recuperar um ponteiro para a interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de um objeto de enumeração.
2.  Passe um PIDL não alocado para [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). **Em seguida** , cuida da alocação do PIDL, mas o aplicativo deve desalocá-lo quando não for mais necessário. Quando **Next** retornar, o PIDL conterá apenas a ID do item do objeto e os caracteres **nulos** de terminação. Em outras palavras, é um PIDL de nível único, em relação à pasta, não a um PIDL totalmente qualificado.
3.  Repita a etapa 2 até [**Avançar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) retornar S \_ false para indicar que todos os itens foram enumerados.
4.  Chame **IEnumIDList:: Release** para liberar o objeto de enumeração.

> [!Note]  
> É importante controlar se você está trabalhando com um PIDL completo ou relativo. Algumas funções e métodos aceitarão qualquer um deles, mas outros terão apenas um ou outro.

 

Os três métodos [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) restantes ([**redefinição**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**ignorar**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)e [**clonagem**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) são úteis se você precisar fazer enumerações repetidas da pasta. Eles permitem que você redefina a enumeração, pule um ou mais objetos e faça uma cópia do objeto de enumeração para preservar seu estado.

## <a name="determining-display-names-and-other-properties"></a>Determinando nomes de exibição e outras propriedades

Depois de enumerar todos os PIDLs que estão contidos em uma pasta, você pode descobrir que tipo de objetos eles representam. A interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) fornece vários métodos úteis, dois dos quais são discutidos aqui. Outros métodos **IShellFolder** e outras interfaces de pasta do Shell serão discutidos posteriormente.

Uma das propriedades mais úteis é o nome de exibição do objeto. Para recuperar o nome de exibição de um objeto, passe seu PIDL para [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Embora o objeto possa estar localizado em qualquer lugar abaixo da pasta pai no namespace, seu PIDL deve ser relativo à pasta.

[**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) retorna o nome de exibição como parte de uma estrutura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Como a extração do nome de exibição de uma estrutura **Strret** pode ser um pouco complicada, o Shell fornece duas funções que fazem o trabalho para você, [**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) e [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa). Ambas as funções usam uma estrutura **Strret** e retornam o nome de exibição como uma cadeia de caracteres normal. Elas diferem apenas em como a cadeia de caracteres é alocada.

Além do seu nome de exibição, um objeto pode ter um número de atributos, como se ele é uma pasta ou se pode ser movido. Você pode recuperar os atributos de um objeto passando seu PIDL para [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof). A lista completa de atributos é muito grande, portanto, você deve ver a referência para obter detalhes. Observe que o PIDL que você passa para **GetAttributesOf** deve ser de nível único. Em particular, **IShellFolder:: GetAttributesOf** aceitará o PIDLs retornado por [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Você pode passar uma matriz de PIDLs e **GetAttributesOf** retornará os atributos que todos os objetos na matriz têm em comum.

Se você tiver um caminho totalmente qualificado do objeto ou PIDL, o [**SHGetFileInfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) fornecerá uma maneira simples de recuperar informações sobre um objeto que seja suficiente para muitas finalidades. **SHGetFileInfo** usa um caminho totalmente qualificado ou PIDL e retorna uma variedade de informações sobre o objeto, incluindo:

-   O nome de exibição do objeto
-   Os atributos do objeto
-   Manipula os ícones do objeto
-   Um identificador para a lista de imagens do sistema
-   O caminho do arquivo que contém o ícone do objeto

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Obtendo um ponteiro para a interface IShellFolder de uma subpasta

Você pode determinar se a pasta contém todas as subpastas chamando [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) e verificando se o sinalizador de \_ pasta SFGAO está definido. Se um objeto for uma pasta, você poderá associá-lo, que fornece um ponteiro para sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Para associar a uma subpasta, chame o método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) da pasta pai. Esse método usa o PIDL da subpasta e retorna um ponteiro para sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Depois de ter esse ponteiro, você pode usar os métodos **IShellFolder** para enumerar o conteúdo das subpastas, determinar suas propriedades e assim por diante.

## <a name="determining-an-objects-parent-folder"></a>Determinando a pasta pai de um objeto

Se você tiver o PIDL de um objeto, talvez seja necessário um identificador para uma das interfaces expostas por sua pasta pai. Por exemplo, se você quiser determinar o nome de exibição associado a um PIDL usando [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), primeiro você deve recuperar a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do pai do objeto. É possível fazer isso com as técnicas discutidas nas seções anteriores. No entanto, uma abordagem muito mais simples é usar a função Shell, [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent). Essa função usa o PIDL totalmente qualificado de um objeto e retorna um ponteiro de interface especificado na pasta pai. Opcionalmente, ele também retorna o PIDL de nível único do item para uso em métodos como [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

O exemplo de aplicativo de console a seguir recupera o PIDL da pasta especial do sistema e retorna seu nome de exibição.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



O aplicativo usa primeiro [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) para recuperar o PIDL da pasta do sistema. Em seguida, ele chama [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent), que retorna um ponteiro para a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta pai e a PIDL da pasta do sistema em relação ao seu pai. Em seguida, ele usa o método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) da pasta pai para recuperar o nome de exibição da pasta do sistema. Como **GetDisplayNameOf** retorna uma estrutura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) é usado para converter o nome de exibição em uma cadeia de caracteres normal. Depois de exibir o nome de exibição, os ponteiros de interface são liberados e o sistema PIDL liberado. Observe que você não deve liberar o PIDL relativo retornado pelo **SHBindToParent**.

 

 
