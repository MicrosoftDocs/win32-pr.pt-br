---
description: Contém o caminho do arquivo de ícone para a conexão.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808245"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="a87d4-103">Elemento ICONFilePath (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="a87d4-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="a87d4-104">O elemento **ICONFilePath (MBNProfile)** contém o caminho do arquivo de ícone para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a87d4-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="a87d4-105">A interface do usuário da conexão do sistema operacional exibirá esse ícone quando uma conexão for feita usando esse elemento.</span><span class="sxs-lookup"><span data-stu-id="a87d4-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="a87d4-106">Ao passar o XML para criar o perfil no método [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) da interface [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , esse caminho deve apontar para o local de origem do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="a87d4-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="a87d4-107">Após a criação bem-sucedida do objeto [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , o serviço de banda larga móvel copiará o arquivo de ícone no repositório interno e o caminho do perfil será modificado para refletir isso.</span><span class="sxs-lookup"><span data-stu-id="a87d4-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="a87d4-108">O arquivo de ícone deve estar no formato. bmp com a dimensão de 32X32 x 32 pixels.</span><span class="sxs-lookup"><span data-stu-id="a87d4-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="a87d4-109">Esse elemento é uma cadeia de caracteres com comprimento de até 1024 caracteres, contendo um caminho de arquivo absoluto.</span><span class="sxs-lookup"><span data-stu-id="a87d4-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="a87d4-110">O elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="a87d4-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="a87d4-111">O elemento **ICONFilePath** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a87d4-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87d4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a87d4-112">Requirements</span></span>



| <span data-ttu-id="a87d4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a87d4-113">Requirement</span></span> | <span data-ttu-id="a87d4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a87d4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a87d4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a87d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a87d4-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a87d4-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a87d4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a87d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a87d4-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a87d4-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a87d4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a87d4-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="a87d4-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a87d4-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a87d4-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="a87d4-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="a87d4-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a87d4-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a87d4-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="a87d4-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




