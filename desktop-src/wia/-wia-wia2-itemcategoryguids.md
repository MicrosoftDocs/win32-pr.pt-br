---
description: Os itens de aquisição de imagem do Windows (WIA) 2,0 são agrupados em categorias que definem como um IWiaItem2 deve ser tratado ou usado.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUIDs de categoria de item WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785162"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="de897-103">GUIDs de categoria de item WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="de897-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="de897-104">Os itens de aquisição de imagem do Windows (WIA) 2,0 são agrupados em categorias que definem como um [**IWiaItem2**](-wia-iwiaitem2.md) deve ser tratado ou usado.</span><span class="sxs-lookup"><span data-stu-id="de897-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="de897-105">Por exemplo, se o item representa um alimentador, o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="de897-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="de897-106">Se o item representa um arquivo concluído, um aplicativo WIA 2,0 deve tratá-lo dessa forma, supondo que os dados sejam estáticos e localizados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de897-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="de897-107">(As regras para cada item serão definidas em seus documentos de especificação individuais.) Cada categoria tem uma constante de tipo GUID.</span><span class="sxs-lookup"><span data-stu-id="de897-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="de897-108">Constante</span><span class="sxs-lookup"><span data-stu-id="de897-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="de897-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="de897-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="de897-110"><dt>**\_automático da categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="de897-111">Um item que representa as definições de configuração automática para um dispositivo de scanner WIA 2,0 que dá suporte à verificação configurada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="de897-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="de897-112"><dt>**\_alimentador de categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="de897-113">Um item do alimentador que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte aos alimentadores de documentos.</span><span class="sxs-lookup"><span data-stu-id="de897-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="de897-114"><dt>**\_voltar do \_ alimentador de categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="de897-115">Uma fonte de dados programável que descreve a fonte de dados do lado de fundo de um item do alimentador base duplex.</span><span class="sxs-lookup"><span data-stu-id="de897-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="de897-116"><dt>**\_frente do \_ alimentador de categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="de897-117">Uma fonte de dados programável que descreve a fonte de dados do Front Side de um item do alimentador base duplex.</span><span class="sxs-lookup"><span data-stu-id="de897-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="de897-118"><dt>**\_filme de categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="de897-119">Um item de filme que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte a unidades de verificação de filmes.</span><span class="sxs-lookup"><span data-stu-id="de897-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="de897-120"><dt>**\_arquivo de categoria WIA \_ concluído \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="de897-121">Um item que não é uma fonte de dados programável ou um item que fornece dados em um formato de arquivo concluído ou um item de pasta que contém itens de formato de arquivo concluído.</span><span class="sxs-lookup"><span data-stu-id="de897-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="de897-122"><dt>**\_superfície da categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="de897-123">Um item de mesa que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte à verificação do cilindro de mesa.</span><span class="sxs-lookup"><span data-stu-id="de897-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="de897-124"><dt>**\_pasta da categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="de897-125">Um item de armazenamento de pasta (não uma fonte de dados programável) que contém outros itens de pasta ou arquivos concluídos ou ambos.</span><span class="sxs-lookup"><span data-stu-id="de897-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="de897-126"><dt>**\_raiz da categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de897-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="de897-127">O item raiz do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de897-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="de897-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de897-128">Requirements</span></span>



| <span data-ttu-id="de897-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="de897-129">Requirement</span></span> | <span data-ttu-id="de897-130">Valor</span><span class="sxs-lookup"><span data-stu-id="de897-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de897-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de897-131">Minimum supported client</span></span><br/> | <span data-ttu-id="de897-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de897-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="de897-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de897-133">Minimum supported server</span></span><br/> | <span data-ttu-id="de897-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de897-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="de897-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de897-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="de897-136"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="de897-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




