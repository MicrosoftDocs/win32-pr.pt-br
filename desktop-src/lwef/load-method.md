---
title: Método Load
description: Método Load
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105784535"
---
# <a name="load-method"></a><span data-ttu-id="60de5-103">Método Load</span><span class="sxs-lookup"><span data-stu-id="60de5-103">Load Method</span></span>

<span data-ttu-id="60de5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60de5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="60de5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="60de5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="60de5-106">Carrega um caractere na coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="60de5-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="60de5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="60de5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="60de5-108">\*agente do ***. Caracteres. Load "*** characterid \* \* *",* \*  *provedor*</span><span class="sxs-lookup"><span data-stu-id="60de5-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="60de5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="60de5-109">Part</span></span>          | <span data-ttu-id="60de5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="60de5-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60de5-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="60de5-111">*CharacterID*</span></span> | <span data-ttu-id="60de5-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="60de5-112">Required.</span></span> <span data-ttu-id="60de5-113">Um valor de cadeia de caracteres que será usado para se referir aos dados de caractere a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="60de5-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="60de5-114">*Provedor*</span><span class="sxs-lookup"><span data-stu-id="60de5-114">*Provider*</span></span>    | <span data-ttu-id="60de5-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="60de5-115">Required.</span></span> <span data-ttu-id="60de5-116">Um tipo de dados Variant que deve ser um dos seguintes: **filespec** o local do arquivo local do arquivo de definição do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="60de5-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="60de5-117">**URL** do O endereço HTTP para o arquivo de definição do caractere.</span><span class="sxs-lookup"><span data-stu-id="60de5-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60de5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="60de5-118">Remarks</span></span>

<span data-ttu-id="60de5-119">Você pode carregar caracteres do subdiretório do agente especificando um caminho relativo (um que não inclui dois pontos ou um caractere de barra à esquerda).</span><span class="sxs-lookup"><span data-stu-id="60de5-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="60de5-120">Isso prefixa o caminho com o diretório de caracteres do agente (localizado no diretório localizado do Windows \\ MSAgent).</span><span class="sxs-lookup"><span data-stu-id="60de5-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="60de5-121">Por exemplo, especificar o seguinte carregaria gênio. ACS do diretório de caracteres do agente:</span><span class="sxs-lookup"><span data-stu-id="60de5-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="60de5-122">Você também pode especificar seu próprio diretório no diretório de caracteres do agente.</span><span class="sxs-lookup"><span data-stu-id="60de5-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="60de5-123">Você pode carregar o caractere definido atualmente como o caractere padrão do usuário atual, não incluindo um caminho como o segundo parâmetro do método **Load** .</span><span class="sxs-lookup"><span data-stu-id="60de5-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="60de5-124">Não é possível carregar o mesmo caractere (um caractere com o mesmo GUID) mais de uma vez a partir de uma única instância do controle.</span><span class="sxs-lookup"><span data-stu-id="60de5-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="60de5-125">Da mesma forma, você não pode carregar o caractere padrão e outros caracteres ao mesmo tempo de uma única instância do controle porque o caractere padrão pode ser o mesmo que o outro caractere.</span><span class="sxs-lookup"><span data-stu-id="60de5-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="60de5-126">Se você tentar fazer isso, o servidor gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="60de5-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="60de5-127">No entanto, você pode criar outra instância do controle Agent e carregar o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="60de5-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="60de5-128">O Provedor de Dados do Microsoft Agent dá suporte ao carregamento de dados de caracteres armazenados como um único arquivo estruturado (. ACS) com dados de caractere e dados de animação juntos ou como dados de caractere separados (. ACF) e animação (. ACA) arquivos.</span><span class="sxs-lookup"><span data-stu-id="60de5-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="60de5-129">Use estrutura única. Arquivo ACS para carregar um caractere que é armazenado em um disco ou rede local e acessado usando um protocolo de arquivo convencional (como caminhos UNC).</span><span class="sxs-lookup"><span data-stu-id="60de5-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="60de5-130">Use a separada. ACF e. ACA arquivos quando você deseja carregar os arquivos de animação individualmente de um site remoto onde eles são acessados usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="60de5-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="60de5-131">Fins. Os arquivos ACS, usando o método **Load** , fornecem acesso às animações de um caractere.</span><span class="sxs-lookup"><span data-stu-id="60de5-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="60de5-132">Fins. Arquivos ACF, você também usa o método [**Get**](get-method.md) para carregar dados de animação.</span><span class="sxs-lookup"><span data-stu-id="60de5-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="60de5-133">O método **Load** não oferece suporte ao download. Arquivos ACS de um site HTTP.</span><span class="sxs-lookup"><span data-stu-id="60de5-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="60de5-134">O carregamento de um caractere não exibe automaticamente o caractere.</span><span class="sxs-lookup"><span data-stu-id="60de5-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="60de5-135">Use o método [**show**](show-method.md) primeiro para tornar o caractere visível.</span><span class="sxs-lookup"><span data-stu-id="60de5-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="60de5-136">Se você usar o método **Load** para carregar um arquivo de caracteres armazenado no computador local e a chamada falhar; por exemplo, como o arquivo não foi encontrado, o Agent gera um erro.</span><span class="sxs-lookup"><span data-stu-id="60de5-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="60de5-137">Você pode usar o suporte em sua linguagem de programação para fornecer uma rotina de tratamento de erros para detectar e processar o erro.</span><span class="sxs-lookup"><span data-stu-id="60de5-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="60de5-138">Você também pode manipular o erro definindo [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) como **false**, declarando um objeto e atribuindo a solicitação de **carregamento** a ele.</span><span class="sxs-lookup"><span data-stu-id="60de5-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="60de5-139">Em seguida, siga a chamada de **carregamento** com uma instrução que verifica o status do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="60de5-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="60de5-140">Se você carregar um caractere que não seja local; por exemplo, usando o protocolo HTTP, você também pode verificar se há uma falha de **carregamento** atribuindo um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) ao método **Load** .</span><span class="sxs-lookup"><span data-stu-id="60de5-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="60de5-141">No entanto, como esse método de carregamento de um caractere é manipulado de forma assíncrona, verifique seu status no evento [**RequestComplete**](requestcomplete-event.md) .</span><span class="sxs-lookup"><span data-stu-id="60de5-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="60de5-142">Essa técnica não funcionará para carregar um caractere usando o protocolo UNC, pois o método **Load** é processado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="60de5-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

