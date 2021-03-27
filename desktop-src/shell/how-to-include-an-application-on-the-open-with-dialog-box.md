---
description: Ilustra como garantir que seu aplicativo aparece no menu abrir com e na caixa de diálogo para aplicativos da área de trabalho e está disponível como um aplicativo padrão da Windows Store para tipos de arquivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Como incluir um aplicativo na caixa de diálogo abrir com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828291"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="0c163-103">Como incluir um aplicativo na caixa de diálogo abrir com</span><span class="sxs-lookup"><span data-stu-id="0c163-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="0c163-104">Ilustra como garantir que seu aplicativo aparece no menu **abrir com** e na caixa de diálogo para aplicativos da área de trabalho e está disponível como um aplicativo padrão da Windows Store para tipos de arquivo especificados.</span><span class="sxs-lookup"><span data-stu-id="0c163-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="0c163-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="0c163-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="0c163-106">Para cada tipo de arquivo, adicione seu aplicativo à subchave do registro OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="0c163-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="0c163-107">Adicione o ProgID como um nome de valor, com o tipo de valor de REG \_ None ou reg \_ sz e uma cadeia de caracteres vazia como o valor de dados.</span><span class="sxs-lookup"><span data-stu-id="0c163-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="0c163-108">Os exemplos de registro a seguir mostram entradas que associam o InfoPath e para Microsoft Visual Studio com o tipo de arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="0c163-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="0c163-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c163-109">Remarks</span></span>

<span data-ttu-id="0c163-110">A subchave **OpenWithProgids** é preferida para **OpenWithList** para identificar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c163-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="0c163-111">Para obter mais informações sobre essas subchaves, consulte [definindo subchaves opcionais e atributos de extensão de tipo de arquivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="0c163-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="0c163-112">O **OpenWithList** é destinado apenas a aplicativos herdados (deve ser. exe somente) em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c163-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



