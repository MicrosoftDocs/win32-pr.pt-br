---
description: As funções que não foram implementadas com uma versão Unicode normalmente foram substituídas por funções mais poderosas ou estendidas que dão suporte a Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usando funções que não têm equivalentes Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172180"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="c7658-103">Usando funções que não têm equivalentes Unicode</span><span class="sxs-lookup"><span data-stu-id="c7658-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="c7658-104">As funções que não foram implementadas com uma versão [Unicode](unicode.md) normalmente foram substituídas por funções mais poderosas ou estendidas que dão suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7658-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="c7658-105">Por exemplo, se você estiver portando um código que chama a função [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , seu aplicativo poderá dar suporte a Unicode usando a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c7658-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="c7658-106">Se uma função não tiver nenhum equivalente Unicode, o aplicativo poderá mapear os caracteres de e para os conjuntos de caracteres de 8 bits antes e depois da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="c7658-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="c7658-107">Por exemplo, as funções de formatação de número **atoi** e **itoa** usam apenas os dígitos de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="c7658-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="c7658-108">Normalmente, o mapeamento de Unicode para caracteres de 8 bits causa perda de dados, mas isso pode ser evitado, tornando o código independente e tornando as expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="c7658-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="c7658-109">As instruções no exemplo a seguir, gravadas para caracteres de 8 bits, são dependentes de tipo e devem ser alteradas para dar suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7658-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="c7658-110">Essas instruções podem ser reescritas da seguinte maneira para torná-las independentes de tipo.</span><span class="sxs-lookup"><span data-stu-id="c7658-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="c7658-111">Neste exemplo, a função de biblioteca C padrão **wcstombs** converte o Unicode em ASCII.</span><span class="sxs-lookup"><span data-stu-id="c7658-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="c7658-112">O exemplo se baseia no fato de que os dígitos de 0 a 9 sempre podem ser traduzidos de Unicode para ASCII, mesmo que parte do texto ao redor não possa.</span><span class="sxs-lookup"><span data-stu-id="c7658-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="c7658-113">A função **atoi** para qualquer caractere que não seja um dígito.</span><span class="sxs-lookup"><span data-stu-id="c7658-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="c7658-114">Seu aplicativo pode usar a função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) do NLS (suporte ao idioma nacional) para processar o texto que inclui os [dígitos nativos](digit-shapes.md) fornecidos para alguns dos scripts em Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7658-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="c7658-115">O uso incorreto da função **wcstombs** pode comprometer a segurança do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7658-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="c7658-116">Verifique se o buffer do aplicativo para a cadeia de caracteres de 8 bits tem pelo menos tamanho 2 \* (*\_ tamanho do caractere* + 1), em que *\_ comprimento do char* representa o comprimento da cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7658-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="c7658-117">Essa restrição é feita porque, com DBCS ( [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) ), cada caractere Unicode pode ser mapeado para dois caracteres consecutivos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c7658-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="c7658-118">Se o buffer não mantiver toda a cadeia de caracteres, a cadeia de caracteres de resultado não será terminada em nulo, apresentando um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="c7658-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="c7658-119">Para obter mais informações sobre segurança de aplicativos, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="c7658-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c7658-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7658-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7658-121">Usando Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="c7658-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
