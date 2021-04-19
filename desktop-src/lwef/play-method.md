---
title: Método play (recursos de ambiente herdado do Windows)
description: Método play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105813225"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="4e902-103">Método play (recursos de ambiente herdado do Windows)</span><span class="sxs-lookup"><span data-stu-id="4e902-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="4e902-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e902-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4e902-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="4e902-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4e902-106">Reproduz a animação especificada para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="4e902-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="4e902-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="4e902-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4e902-108">\*Agente \***. Caracteres ("**_characterid_*_"). Reproduzir_* "*animationname*"</span><span class="sxs-lookup"><span data-stu-id="4e902-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="4e902-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4e902-109">Part</span></span>            | <span data-ttu-id="4e902-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e902-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="4e902-111">*Animaçãoname*</span><span class="sxs-lookup"><span data-stu-id="4e902-111">*AnimationName*</span></span> | <span data-ttu-id="4e902-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4e902-112">Required.</span></span> <span data-ttu-id="4e902-113">Uma cadeia de caracteres que especifica o nome de uma sequência de animação.</span><span class="sxs-lookup"><span data-stu-id="4e902-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e902-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e902-114">Remarks</span></span>

<span data-ttu-id="4e902-115">O nome de uma animação é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4e902-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4e902-116">Antes de reproduzir a animação especificada, o servidor tentará reproduzir a animação de **retorno** para a animação anterior, se uma tiver sido atribuída.</span><span class="sxs-lookup"><span data-stu-id="4e902-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="4e902-117">Ao acessar as animações de um caractere usando um protocolo de arquivo convencional, você pode simplesmente usar o método **Play** especificando o nome da animação.</span><span class="sxs-lookup"><span data-stu-id="4e902-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="4e902-118">No entanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método **Get** para carregar a animação antes de chamar o método **Play** .</span><span class="sxs-lookup"><span data-stu-id="4e902-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="4e902-119">Para obter mais informações, consulte o método **Get** .</span><span class="sxs-lookup"><span data-stu-id="4e902-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="4e902-120">Para simplificar a sintaxe, você pode declarar uma referência de objeto e defini-la para fazer referência ao objeto [**Character**](/windows/desktop/lwef/the-characters-object) na coleção [**Characters**](/windows/desktop/lwef/the-characters-object) e usar a referência como parte de suas instruções **Play** :</span><span class="sxs-lookup"><span data-stu-id="4e902-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="4e902-121">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="4e902-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="4e902-122">Além disso, se você especificar uma animação que não está carregada ou se o caractere não tiver sido carregado com êxito, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="4e902-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="4e902-123">No entanto, se a animação não existir e os dados do caractere já tiverem sido carregados com êxito, o servidor gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="4e902-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="4e902-124">O método **Play** não torna o caractere visível.</span><span class="sxs-lookup"><span data-stu-id="4e902-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="4e902-125">Se o caractere não estiver visível, o servidor reproduzirá a animação de forma invisível e definirá a propriedade [**status**](status-property.md) do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="4e902-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
