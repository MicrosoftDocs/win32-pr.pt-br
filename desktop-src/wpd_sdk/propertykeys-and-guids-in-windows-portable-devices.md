---
description: PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829083"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="5ef8c-103">PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="5ef8c-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="5ef8c-104">Uma propriedade ou comando é identificado por uma estrutura PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="5ef8c-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="5ef8c-105">Uma estrutura PROPERTYKEY é composta de duas partes: um GUID (o membro fmtid) e um DWORD (o membro PID).</span><span class="sxs-lookup"><span data-stu-id="5ef8c-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="5ef8c-106">A parte GUID é usada para indicar a categoria à qual a propriedade ou o comando pertence (ou seja, propriedades relacionadas pertencem à mesma categoria e os comandos relacionados pertencem à mesma categoria; portanto, eles terão o mesmo fmtid).</span><span class="sxs-lookup"><span data-stu-id="5ef8c-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="5ef8c-107">A parte DWORD indica a propriedade ou a ID de comando e é usada para distinguir as propriedades ou comandos individuais dentro de uma categoria de propriedade ou comando (ou seja, os valores de PID para propriedades ou comandos na mesma categoria serão diferentes).</span><span class="sxs-lookup"><span data-stu-id="5ef8c-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="5ef8c-108">A seção de referência deste documento descreve todos os valores de PROPERTYKEY definidos por WPD; esses valores correspondem a comandos, propriedades e recursos.</span><span class="sxs-lookup"><span data-stu-id="5ef8c-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="5ef8c-109">Se você criar um valor de PROPERTYKEY personalizado, deverá definir uma nova categoria de **GUID** ; Não reutilize os valores de **GUID** WPD ou você correrá o risco de entrar em conflito com o PROPERTYKEYs especificado por WPD existente e futuro.</span><span class="sxs-lookup"><span data-stu-id="5ef8c-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ef8c-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ef8c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef8c-111">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="5ef8c-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="5ef8c-112">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="5ef8c-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="5ef8c-113">**GUIDs de formato de objeto**</span><span class="sxs-lookup"><span data-stu-id="5ef8c-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="5ef8c-114">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="5ef8c-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ef8c-115">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="5ef8c-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



