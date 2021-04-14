---
description: Especifica se este é o perfil padrão para o dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461086"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="99b1e-103">Elemento IsDefault (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="99b1e-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="99b1e-104">O elemento **IsDefault (MBNProfile)** especifica se esse é o perfil padrão para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99b1e-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="99b1e-105">Esse é um elemento opcional e, se não for especificado, o perfil não será definido como o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="99b1e-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="99b1e-106">O perfil padrão é usado pelo serviço de banda larga móvel para os seguintes fins</span><span class="sxs-lookup"><span data-stu-id="99b1e-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="99b1e-107">O serviço de banda larga móvel usa as configurações de conexão do perfil padrão ao executar conexões de rede automáticas.</span><span class="sxs-lookup"><span data-stu-id="99b1e-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="99b1e-108">Essas configurações incluem nome do ponto de acesso, nome de usuário, senha, etc.</span><span class="sxs-lookup"><span data-stu-id="99b1e-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="99b1e-109">A política de conexão automática para um dispositivo de banda larga móvel é obtida do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="99b1e-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="99b1e-110">A interface do usuário da conexão de rede do sistema operacional também usa dados de conexão do perfil padrão para operações de conexão.</span><span class="sxs-lookup"><span data-stu-id="99b1e-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="99b1e-111">Os provedores de serviços de celular podem fornecer os detalhes de conexão em um perfil e configurar esse perfil como um perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="99b1e-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="99b1e-112">O serviço de banda larga móvel usará essas configurações de conexão sem avisar o usuário para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="99b1e-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="99b1e-113">O elemento **IsDefault** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="99b1e-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b1e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b1e-114">Requirements</span></span>



| <span data-ttu-id="99b1e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b1e-115">Requirement</span></span> | <span data-ttu-id="99b1e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="99b1e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="99b1e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b1e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="99b1e-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99b1e-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="99b1e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b1e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="99b1e-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="99b1e-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="99b1e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="99b1e-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="99b1e-122">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="99b1e-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="99b1e-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="99b1e-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="99b1e-124">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="99b1e-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="99b1e-125">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="99b1e-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




