---
description: Você não pode criar instâncias das classes corrigidas no namespace localizado. As classes corrigidas no namespace localizado são tratadas como se fossem abstratas, embora não contenham o qualificador abstract.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerações sobre a classe corrigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172304"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="17c5b-104">Considerações sobre a classe corrigida</span><span class="sxs-lookup"><span data-stu-id="17c5b-104">Amended Class Considerations</span></span>

<span data-ttu-id="17c5b-105">Você não pode criar instâncias das classes corrigidas no namespace localizado.</span><span class="sxs-lookup"><span data-stu-id="17c5b-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="17c5b-106">As classes corrigidas no namespace localizado são tratadas como se fossem abstratas, embora não contenham o qualificador [**abstract**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="17c5b-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="17c5b-107">Se você recuperar uma classe corrigida de um namespace localizado usando o \_ sinalizador WBEM \_ usar \_ sinalizador de \_ qualificadores corrigidos e gerar uma instância a partir dele, a instância conterá todos os qualificadores corrigidos da classe corrigida.</span><span class="sxs-lookup"><span data-stu-id="17c5b-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="17c5b-108">Não é possível armazenar essa nova classe no namespace que contém a definição de classe básica, a menos que você execute a operação **Put** com o sinalizador WBEM \_ \_ usar \_ sinalizador de \_ qualificadores corrigidos.</span><span class="sxs-lookup"><span data-stu-id="17c5b-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="17c5b-109">Esse sinalizador instrui o WMI a remover quaisquer qualificadores reparados antes de salvar o objeto.</span><span class="sxs-lookup"><span data-stu-id="17c5b-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="17c5b-110">Se você não especificar \_ o sinalizador WBEM \_ usar \_ \_ qualificadores corrigidos, a operação **Put** falhará com um erro de objeto do WBEM \_ E \_ alterado \_ .</span><span class="sxs-lookup"><span data-stu-id="17c5b-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



