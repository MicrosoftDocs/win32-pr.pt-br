---
title: Atributos do MultiPoint no WSAPROTOCOL_INFO
description: Os atributos do MultiPoint na \_ estrutura de informações do WSAPROTOCOL incluem XP1 \_ \_ MULTIPONTO MultiPoint, XP1 \_ MultiPoint \_ Control \_ plano e XP1 \_ MultiPoint \_ Data \_ Plane.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647134"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="dd170-103">Atributos do MultiPoint no WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="dd170-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="dd170-104">Três parâmetros de atributo são definidos na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir os diferentes esquemas usados nos planos de controle e de dados, respectivamente:</span><span class="sxs-lookup"><span data-stu-id="dd170-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="dd170-105">XP1 \_ suporte \_ a MultiPoint com um valor de 1 indica que essa entrada de protocolo dá suporte a comunicações do MultiPoint e que os dois parâmetros a seguir são significativos.</span><span class="sxs-lookup"><span data-stu-id="dd170-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="dd170-106">\_ \_ \_ O plano de controle do MultiPoint XP1 indica se o plano de controle tem raiz (valor = 1) ou não raiz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="dd170-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="dd170-107">\_ \_ \_ O plano de dados do MultiPoint XP1 indica se o plano de dados tem raiz (valor = 1) ou não raiz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="dd170-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="dd170-108">Duas entradas de [**\_ informações WSAPROTOCOLs**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarão presentes se um protocolo multiponto suportasse os planos de dados com e sem raiz, uma entrada para cada um.</span><span class="sxs-lookup"><span data-stu-id="dd170-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
