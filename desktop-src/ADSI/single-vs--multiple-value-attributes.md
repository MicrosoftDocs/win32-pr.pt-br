---
title: Atributos únicos versus múltiplos valores
description: Os atributos que podem existir em um diretório são normalmente definidos no esquema para o diretório.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI de atributos de valor único vs. Multiple
- atributos ADSI, simples versus vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004855"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="9769c-105">Atributos únicos versus múltiplos valores</span><span class="sxs-lookup"><span data-stu-id="9769c-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="9769c-106">Os atributos que podem existir em um diretório são normalmente definidos no esquema para o diretório.</span><span class="sxs-lookup"><span data-stu-id="9769c-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="9769c-107">A definição de esquema de um atributo especifica um número de características do atributo, como o tipo de dados e se uma instância do atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="9769c-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="9769c-108">Uma instância de um atributo de valor único pode conter um único valor.</span><span class="sxs-lookup"><span data-stu-id="9769c-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="9769c-109">Uma instância de um atributo de múltiplos valores pode conter um único valor ou vários valores.</span><span class="sxs-lookup"><span data-stu-id="9769c-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="9769c-110">Active Directory não cria atributos com valores vazios — ou o atributo contém um valor válido ou não existe no objeto.</span><span class="sxs-lookup"><span data-stu-id="9769c-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="9769c-111">No Active Directory e a maioria dos outros servidores LDAP, a ordem dos valores em um atributo com valores múltiplos é indefinida.</span><span class="sxs-lookup"><span data-stu-id="9769c-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="9769c-112">Além disso, cada valor de um atributo com valores múltiplos deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9769c-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="9769c-113">A ADSI normalmente carrega dados de esquema se o diretório der suporte a um esquema, como Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9769c-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="9769c-114">Como a ADSI conhece a sintaxe dos atributos no esquema, não é necessário especificar o tipo de atributo ao acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="9769c-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="9769c-115">A ADSI realiza marshaling de valores de atributo para o tipo de dados apropriado, conforme definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="9769c-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="9769c-116">Se o diretório não tiver nenhum esquema, forneça o tipo de dados ao acessar um atributo.</span><span class="sxs-lookup"><span data-stu-id="9769c-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="9769c-117">Active Directory, Exchange, Windows NT 4,0 e servidor do site têm um esquema.</span><span class="sxs-lookup"><span data-stu-id="9769c-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="9769c-118">Além disso, Active Directory tem um esquema extensível.</span><span class="sxs-lookup"><span data-stu-id="9769c-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




