---
title: IAgent carga
description: IAgent carga
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917282"
---
# <a name="iagentload"></a><span data-ttu-id="9e81c-103">IAgent:: Load</span><span class="sxs-lookup"><span data-stu-id="9e81c-103">IAgent::Load</span></span>

<span data-ttu-id="9e81c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e81c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="9e81c-105">Carrega um caractere na coleção de [**caracteres**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="9e81c-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="9e81c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9e81c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9e81c-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="9e81c-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="9e81c-108">Um tipo de dados Variant que deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="9e81c-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e81c-109">*filespec*</span><span class="sxs-lookup"><span data-stu-id="9e81c-109">*filespec*</span></span> | <span data-ttu-id="9e81c-110">O local do arquivo local do arquivo de definição do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="9e81c-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="9e81c-111">*URL*</span><span class="sxs-lookup"><span data-stu-id="9e81c-111">*URL*</span></span>      | <span data-ttu-id="9e81c-112">O endereço HTTP para o arquivo de definição do caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="9e81c-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="9e81c-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="9e81c-114">Endereço de uma variável que recebe a ID do caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="9e81c-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="9e81c-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="9e81c-116">Endereço de uma variável que recebe a ID da solicitação de [**carregamento**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="9e81c-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="9e81c-117">Você pode carregar caracteres do subdiretório do Microsoft Agent especificando um caminho relativo (um que não inclua dois pontos ou um caractere de barra à esquerda).</span><span class="sxs-lookup"><span data-stu-id="9e81c-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="9e81c-118">Isso prefixa o caminho com o diretório de caracteres do agente (localizado no diretório% Windows% \\ MSAgent localizado).</span><span class="sxs-lookup"><span data-stu-id="9e81c-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="9e81c-119">Você também pode usar um endereço relativo para especificar seu próprio diretório no diretório de caracteres do agente.</span><span class="sxs-lookup"><span data-stu-id="9e81c-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="9e81c-120">Não é possível carregar o mesmo caractere (um caractere com o mesmo GUID) mais de uma vez a partir de uma única conexão.</span><span class="sxs-lookup"><span data-stu-id="9e81c-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="9e81c-121">Da mesma forma, você não pode carregar o caractere padrão e outros caracteres ao mesmo tempo de uma única conexão, porque o caractere padrão pode ser o mesmo que o outro caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="9e81c-122">No entanto, você pode criar outra conexão (usando CoCreateInstance) e carregar o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="9e81c-123">O provedor de dados do Microsoft Agent dá suporte ao carregamento de dados de caracteres armazenados como um único arquivo estruturado (. ACS) com dados de caractere e dados de animação juntos, ou como dados de caractere separados (. ACF) e animação (. ACA) arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e81c-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="9e81c-124">Em geral, use a estrutura única. Arquivo ACS para carregar um caractere que é armazenado em uma unidade de disco ou rede local e acessado usando o protocolo de arquivo convencional (como caminhos UNC).</span><span class="sxs-lookup"><span data-stu-id="9e81c-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="9e81c-125">Use a separada. ACF e. ACA arquivos quando você deseja carregar os arquivos de animação individualmente de um site remoto onde eles são acessados usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e81c-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="9e81c-126">Fins. Os arquivos ACS, usando o método [**Load**](load-method.md) , fornecem acesso às animações de um caractere; Depois de carregado, você pode usar o método [**Play**](play-method.md) para animar o caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="9e81c-127">Fins. Arquivos ACF, você também usa o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para carregar dados de animação.</span><span class="sxs-lookup"><span data-stu-id="9e81c-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="9e81c-128">O método **Load** não oferece suporte ao download. Arquivos ACS de um site HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e81c-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="9e81c-129">O carregamento de um caractere não exibe automaticamente o caractere.</span><span class="sxs-lookup"><span data-stu-id="9e81c-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="9e81c-130">Use o método [**show**](show-method.md) primeiro para tornar o caractere visível.</span><span class="sxs-lookup"><span data-stu-id="9e81c-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 