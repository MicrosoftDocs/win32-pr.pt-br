---
title: ISAN
description: O atributo ISAN contém o número de audiovisual internacional padrão (ISAN) que identifica o conteúdo.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de mídia do Windows do ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365661"
---
# <a name="isan"></a><span data-ttu-id="d8a5f-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="d8a5f-104">ISAN</span></span>

<span data-ttu-id="d8a5f-105">O atributo **Isan** contém o número de audiovisual internacional padrão (Isan) que identifica o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d8a5f-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="d8a5f-106">Global Constant</span></span>

<span data-ttu-id="d8a5f-107">g \_ wszISAN</span><span class="sxs-lookup"><span data-stu-id="d8a5f-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="d8a5f-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d8a5f-108">Data Type</span></span>

<span data-ttu-id="d8a5f-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d8a5f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a5f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8a5f-110">Remarks</span></span>

<span data-ttu-id="d8a5f-111">O ISAN é um padrão internacional para identificar o audiovisual Works.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="d8a5f-112">Para obter informações sobre o ISAN, visite o [site da Web](https://www.isan.org/)do padrão.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="d8a5f-113">O objeto editor de metadados verifica a cadeia de caracteres de ISAN quando você define esse atributo.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="d8a5f-114">A formatação de cadeia de caracteres aceitável, conforme descrito na seção 4,1 da especificação de ISAN, consiste em 16 dígitos hexadecimais, opcionalmente separados por espaços em branco ou hifens em segmentos de 4 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="d8a5f-115">O número formatado deve ser seguido, opcionalmente separado por um espaço ou hífen, por um caractere de verificação válido.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="d8a5f-116">O caractere de verificação pode ser um dígito decimal ou uma letra maiúscula.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="d8a5f-117">Consulte anexo a do guia do usuário do ISAN para obter informações sobre como derivar o número do cheque.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="d8a5f-118">A cadeia de caracteres de ISAN padrão pode ser seguida pelas informações de versão.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="d8a5f-119">Se houver, as informações de versão consistem em oito dígitos hexadecimais seguidos de um número de cheque.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="d8a5f-120">A formatação desses caracteres segue as mesmas regras que a cadeia de caracteres básica.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="d8a5f-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8a5f-121">Examples</span></span>

<span data-ttu-id="d8a5f-122">A seguir estão três cadeias de caracteres formatadas de forma aceita para um exemplo de ISAN.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="d8a5f-123">A cadeia de caracteres a seguir mostra o formato de um ISAN com informações de versão.</span><span class="sxs-lookup"><span data-stu-id="d8a5f-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="d8a5f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8a5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a5f-125">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="d8a5f-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




