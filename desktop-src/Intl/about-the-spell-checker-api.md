---
description: Para os usuários em todo o mundo, a entrada textual faz parte de uma experiência de computação moderna, para Blogs, comentários, tweeting, mensagens instantâneas ou qualquer outro tipo de digitação de texto. No Windows 8, a verificação ortográfica é interna para editar controles.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Sobre a API de verificação ortográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829017"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="14362-104">Sobre a API de verificação ortográfica</span><span class="sxs-lookup"><span data-stu-id="14362-104">About the Spell Checking API</span></span>

<span data-ttu-id="14362-105">Para os usuários em todo o mundo, a entrada textual faz parte de uma experiência de computação moderna, para Blogs, comentários, tweeting, mensagens instantâneas ou qualquer outro tipo de digitação de texto.</span><span class="sxs-lookup"><span data-stu-id="14362-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="14362-106">No Windows 8, a verificação ortográfica é interna para editar controles.</span><span class="sxs-lookup"><span data-stu-id="14362-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="14362-107">Os desenvolvedores podem usar a API de verificação ortográfica em seus aplicativos para consumir os serviços de verificação ortográfica disponíveis.</span><span class="sxs-lookup"><span data-stu-id="14362-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="14362-108">Os desenvolvedores também podem criar verificadores ortográficos que se tornam provedores e são integrados à estrutura de verificação ortográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="14362-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="14362-109">A API de verificação ortográfica foi projetada para uso por desenvolvedores Professional C/C++ de aplicativos COM (Windows Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="14362-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="14362-110">Não há suporte para a API de verificação ortográfica para uso em um serviço Windows ou ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="14362-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="14362-111">Controle de versão</span><span class="sxs-lookup"><span data-stu-id="14362-111">Versioning</span></span>

<span data-ttu-id="14362-112">A API de verificação ortográfica está disponível a partir do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="14362-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="14362-113">Adições futuras à API serão tratadas pela criação de novas interfaces que podem ser determinadas usando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nos existentes.</span><span class="sxs-lookup"><span data-stu-id="14362-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="14362-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="14362-114">Interfaces</span></span>

<span data-ttu-id="14362-115">Todas as interfaces devem ser liberadas quando não forem mais usadas.</span><span class="sxs-lookup"><span data-stu-id="14362-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="14362-116">Todas as cadeias de caracteres **LPWSTR** (de saída de parâmetro) retornadas (e itens **LPOLESTR** de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devem ser liberadas com [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quando não forem mais usadas.</span><span class="sxs-lookup"><span data-stu-id="14362-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="14362-117">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="14362-117">Error handling</span></span>

<span data-ttu-id="14362-118">Os erros são retornados como **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="14362-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="14362-119">Não há suporte para [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) nesta API.</span><span class="sxs-lookup"><span data-stu-id="14362-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="14362-120">Os erros não são particularmente acionáveis, exceto argumentos incorretos.</span><span class="sxs-lookup"><span data-stu-id="14362-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="14362-121">Os códigos de erro RPC padrão podem ser retornados por qualquer uma das chamadas à API porque estão fora do processo.</span><span class="sxs-lookup"><span data-stu-id="14362-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="14362-122">O tempo limite de RPC padrão é aplicável.</span><span class="sxs-lookup"><span data-stu-id="14362-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="14362-123">Segurança</span><span class="sxs-lookup"><span data-stu-id="14362-123">Security</span></span>

<span data-ttu-id="14362-124">A API de verificação ortográfica pode carregar código externo (provedores de verificação ortográfica).</span><span class="sxs-lookup"><span data-stu-id="14362-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="14362-125">Ele executará esse código fora do processo e sob um contexto de segurança restrito.</span><span class="sxs-lookup"><span data-stu-id="14362-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="14362-126">Arquivos de dicionário</span><span class="sxs-lookup"><span data-stu-id="14362-126">Dictionary files</span></span>

<span data-ttu-id="14362-127">Os dicionários específicos do usuário para um idioma, que armazenam o conteúdo das listas de palavras que foram adicionadas, excluídas e de AutoCorreção, estão localizados em% AppData% \\ Microsoft \\ Spelling \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="14362-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="14362-128">Os nomes de FileName são Default. DIC (adicionado), Default. exc (excluído) e default. ACL (AutoCorreção).</span><span class="sxs-lookup"><span data-stu-id="14362-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="14362-129">Os arquivos são texto não criptografado UTF-16 LE que devem começar com a BOM (marca de ordem de byte) apropriada.</span><span class="sxs-lookup"><span data-stu-id="14362-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="14362-130">Cada linha contém uma palavra (nas listas de palavras adicionadas e excluídas) ou um par de AutoCorreção com as palavras separadas por uma barra vertical (" \| ") (na lista de palavras de AutoCorreção).</span><span class="sxs-lookup"><span data-stu-id="14362-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="14362-131">Outros arquivos. dic,. exc e. ACL presentes no diretório serão detectados pelo serviço de verificação ortográfica e adicionados às listas de palavras do usuário.</span><span class="sxs-lookup"><span data-stu-id="14362-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="14362-132">Esses arquivos são considerados somente leitura e não são modificados pela API de verificação ortográfica.</span><span class="sxs-lookup"><span data-stu-id="14362-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="14362-133">Instalando um provedor de verificação ortográfica</span><span class="sxs-lookup"><span data-stu-id="14362-133">Installing a spell checking provider</span></span>

<span data-ttu-id="14362-134">A instalação de um provedor de verificação ortográfica deve posicionar todos os arquivos que ele usa em um local que permita acesso de leitura do SID ([identificador de segurança](../secauthz/security-identifiers.md)) "todos os pacotes de aplicativos".</span><span class="sxs-lookup"><span data-stu-id="14362-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="14362-135">Instalá-lo em uma pasta em "arquivos de programas" funciona bem.</span><span class="sxs-lookup"><span data-stu-id="14362-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="14362-136">Além disso, o provedor deve definir algumas chaves no registro para que ele apareça para a API de verificação ortográfica.</span><span class="sxs-lookup"><span data-stu-id="14362-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="14362-137">Ele pode estar no hive do \_ usuário atual do hKey \_ ou no \_ hive do computador local hKey \_ , dependendo se ele deve ser instalado somente para o usuário atual ou para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="14362-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="14362-138">O [exemplo de provedor de verificação ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fornece um exemplo do registro necessário para instalar um provedor.</span><span class="sxs-lookup"><span data-stu-id="14362-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="14362-139">Se você estiver criando novas opções de verificação ortográfica para um provedor de verificação ortográfica, consulte [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) para obter orientação sobre nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="14362-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14362-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14362-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14362-141">Referência de API de verificação ortográfica</span><span class="sxs-lookup"><span data-stu-id="14362-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="14362-142">Exemplo de cliente de verificação ortográfica</span><span class="sxs-lookup"><span data-stu-id="14362-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="14362-143">Exemplo de provedor de verificação ortográfica</span><span class="sxs-lookup"><span data-stu-id="14362-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="14362-144">**IOptionDescription:: ID**</span><span class="sxs-lookup"><span data-stu-id="14362-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="14362-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="14362-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="14362-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="14362-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
