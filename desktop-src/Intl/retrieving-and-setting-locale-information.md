---
description: Recuperando e definindo informações de localidade
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperando e definindo informações de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758137"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="72690-103">Recuperando e definindo informações de localidade</span><span class="sxs-lookup"><span data-stu-id="72690-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="72690-104">O aplicativo deve ser capaz de recuperar e definir informações específicas sobre [localidades e idiomas](locales-and-languages.md)disponíveis.</span><span class="sxs-lookup"><span data-stu-id="72690-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="72690-105">Cada elemento de informações de localidade, como o nome de um dia específico da semana ou o caractere usado como separador decimal, tem uma constante correspondente.</span><span class="sxs-lookup"><span data-stu-id="72690-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="72690-106">As constantes disponíveis são definidas nas [constantes de informações de localidade](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="72690-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="72690-107">Seu aplicativo sempre armazena e manipula informações de localidade como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="72690-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="72690-108">Nenhum dado binário é permitido e todos os valores numéricos devem ser especificados como texto.</span><span class="sxs-lookup"><span data-stu-id="72690-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="72690-109">Cada tipo de informação tem um formato específico.</span><span class="sxs-lookup"><span data-stu-id="72690-109">Each type of information has a particular format.</span></span> <span data-ttu-id="72690-110">Além disso, vários tipos são vinculados para que a alteração de um tipo também altere o valor do outro tipo.</span><span class="sxs-lookup"><span data-stu-id="72690-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="72690-111">Para recuperar informações de localidade, o aplicativo chama [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante que corresponde às informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="72690-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="72690-112">O aplicativo pode chamar [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) para definir um item de informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="72690-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="72690-113">Embora um [identificador de localidade](locale-identifiers.md) possa ter suporte, ele não estará disponível para uso por um aplicativo, a menos que a localidade correspondente também esteja instalada.</span><span class="sxs-lookup"><span data-stu-id="72690-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="72690-114">Como a maioria das constantes de informações de localidade é mutuamente exclusiva, apenas um tipo de informação pode ser manipulado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="72690-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="72690-115">As exceções a essa regra são a [localidade \_ usar \_ CP \_ ACP](locale-use-cp-acp.md), [ \_ \_ número de retorno de localidade](locale-return-constants.md)e [ \_ NOUSEROVERRIDE de localidade](locale-nouseroverride.md), que podem ser combinados com outras constantes usando um binário ou.</span><span class="sxs-lookup"><span data-stu-id="72690-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="72690-116">O uso de \_ NOUSEROVERRIDE de localidade é fortemente desencorajado, pois desabilita as preferências do usuário.</span><span class="sxs-lookup"><span data-stu-id="72690-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="72690-117">Como uma série de aplicativos, por exemplo, o Microsoft Active Directory, seu aplicativo pode manter suas cadeias de caracteres em um banco de dados classificável.</span><span class="sxs-lookup"><span data-stu-id="72690-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="72690-118">Para obter mais informações, consulte [lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="72690-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72690-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72690-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72690-120">Usando o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="72690-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="72690-121">Constantes de informações de localidade</span><span class="sxs-lookup"><span data-stu-id="72690-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="72690-122">Lidando com a classificação em seus aplicativos</span><span class="sxs-lookup"><span data-stu-id="72690-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="72690-123">Trabalhando com localidades personalizadas</span><span class="sxs-lookup"><span data-stu-id="72690-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 



