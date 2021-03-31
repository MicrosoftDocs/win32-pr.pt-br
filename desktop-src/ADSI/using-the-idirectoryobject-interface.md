---
title: Usando a interface IDirectoryObject
description: Quando você cria um cliente ADSI em C ou C++ que usa associação inicial, você terá uma variedade maior de tipos de dados ADSI disponíveis para uso para o cliente se ele chamar a interface IDirectoryObject em vez da interface IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, usando
- ADSI da ADSI, usando, usando a interface IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634854"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="124dd-105">Usando a interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="124dd-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="124dd-106">Quando você cria um cliente ADSI em C ou C++ que usa associação inicial, você terá uma variedade maior de tipos de dados ADSI disponíveis para uso para o cliente se ele chamar a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) em vez da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="124dd-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="124dd-107">A interface **IDirectoryObject** fornece métodos para dar suporte a um subconjunto de propriedades de manutenção de um objeto e acessar seus atributos.</span><span class="sxs-lookup"><span data-stu-id="124dd-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="124dd-108">A figura a seguir mostra as relações entre as estruturas de dados.</span><span class="sxs-lookup"><span data-stu-id="124dd-108">The following figure shows the relationships among the data structures.</span></span>

![estruturas de dados da interface idirectoryobject](images/ds2dso.png)

<span data-ttu-id="124dd-110">Na figura anterior, as [**\_ \_ informações de objeto de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_object_info) de estrutura definem propriedades que identificam o objeto por nome distinto, nome distinto relativo, por contêiner (ParentDN), por tipo de objeto (ClassDN) e por definição de esquema (SchemaDN).</span><span class="sxs-lookup"><span data-stu-id="124dd-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="124dd-111">O descritor de atributo [**ADS \_ \_ informações attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consiste em um nome, um tipo de dados, uma matriz de valores de dados mostrados em [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)e um sinalizador que direciona o serviço de diretório subjacente para executar determinadas operações nos atributos detalhados nas [ \_ \_ \* constantes attr do ADS](adsi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="124dd-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="124dd-112">Os tipos de dados desses atributos incluem os tipos de sintaxe estendida ADSI, detalhados em [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span><span class="sxs-lookup"><span data-stu-id="124dd-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




