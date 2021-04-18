---
description: Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag constantes de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789465"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="74b54-103">Bit-Flag constantes de dados</span><span class="sxs-lookup"><span data-stu-id="74b54-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="74b54-104">Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados.</span><span class="sxs-lookup"><span data-stu-id="74b54-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="74b54-105">Como a maioria das constantes de sinalizador de bits é **DWORD** s, um número específico de bits inferiores geralmente é reservado para extensões comuns, enquanto os bits superiores restantes estão disponíveis para extensões específicas do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="74b54-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="74b54-106">Os sinalizadores de bits comuns são atribuídos do bit zero para cima e as extensões específicas do fornecedor devem ser atribuídas do bit 31 para baixo.</span><span class="sxs-lookup"><span data-stu-id="74b54-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="74b54-107">Esse esquema fornece flexibilidade máxima na atribuição de posições de bits a extensões comuns, em oposição às extensões específicas do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="74b54-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="74b54-108">Um fornecedor deve definir novos valores que são extensões naturais dos sinalizadores de bits definidos pela API.</span><span class="sxs-lookup"><span data-stu-id="74b54-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="74b54-109">Estruturas de dados extensíveis têm um campo de tamanho de variavelmente reservado para uso específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74b54-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="74b54-110">Como o campo é dimensionado de forma variada, o provedor de serviços decide a quantidade de informações e interpretação do campo.</span><span class="sxs-lookup"><span data-stu-id="74b54-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="74b54-111">Um fornecedor que define um campo específico do dispositivo deve fazer essas extensões naturais da estrutura de dados original definida pela API.</span><span class="sxs-lookup"><span data-stu-id="74b54-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



