---
title: Método think
description: Método think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823720"
---
# <a name="think-method"></a><span data-ttu-id="0c77c-103">Método think</span><span class="sxs-lookup"><span data-stu-id="0c77c-103">Think Method</span></span>

<span data-ttu-id="0c77c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c77c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c77c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="0c77c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c77c-106">Exibe o texto especificado para o caractere especificado em um balão de palavras "pensamento".</span><span class="sxs-lookup"><span data-stu-id="0c77c-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="0c77c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="0c77c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c77c-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Think* o \*  \[ *texto*\]</span><span class="sxs-lookup"><span data-stu-id="0c77c-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="0c77c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0c77c-109">Part</span></span>   | <span data-ttu-id="0c77c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c77c-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="0c77c-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="0c77c-111">*Text*</span></span> | <span data-ttu-id="0c77c-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0c77c-112">Optional.</span></span> <span data-ttu-id="0c77c-113">Uma cadeia de caracteres que especifica a saída de pensamento do caractere.</span><span class="sxs-lookup"><span data-stu-id="0c77c-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c77c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c77c-114">Remarks</span></span>

<span data-ttu-id="0c77c-115">Como o método [**Speak**](speak-method.md) , o método **Think** é uma solicitação em fila que exibe texto em um balão de palavras, exceto pelo fato de que o balão de palavras de **reflexão** difere visualmente.</span><span class="sxs-lookup"><span data-stu-id="0c77c-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="0c77c-116">Além disso, o balão dá suporte apenas à marca de controle de fala de indicador (**\\ mrk**) e ignora quaisquer outras marcas de controle de fala.</span><span class="sxs-lookup"><span data-stu-id="0c77c-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="0c77c-117">Ao contrário do que se **fala**, o método **Think** não altera o estado de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="0c77c-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="0c77c-118">As propriedades do objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) afetam a saída dos métodos [**Speak**](speak-method.md) e **Think** .</span><span class="sxs-lookup"><span data-stu-id="0c77c-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="0c77c-119">Por exemplo, a propriedade [**Enabled**](enabled-property.md) do objeto **Balloon** deve ser **true** para que o texto seja exibido.</span><span class="sxs-lookup"><span data-stu-id="0c77c-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="0c77c-120">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="0c77c-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="0c77c-121">Além disso, se o arquivo não tiver sido carregado, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="0c77c-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="0c77c-122">A quebra automática de palavras do agente no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço ou tabulação).</span><span class="sxs-lookup"><span data-stu-id="0c77c-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="0c77c-123">No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão.</span><span class="sxs-lookup"><span data-stu-id="0c77c-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="0c77c-124">Em linguagens como japonês, chinês e tailandês em que os espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.</span><span class="sxs-lookup"><span data-stu-id="0c77c-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="0c77c-125">Defina a ID do idioma do caractere antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro do balão do Word.</span><span class="sxs-lookup"><span data-stu-id="0c77c-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 