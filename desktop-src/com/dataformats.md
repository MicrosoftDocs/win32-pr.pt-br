---
title: Formatos de dataformativos
description: Especifica os formatos de dados padrão e principal com suporte por um aplicativo.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Chave do registro COM de dataformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782506"
---
# <a name="dataformats"></a><span data-ttu-id="536e3-104">Formatos de dataformativos</span><span class="sxs-lookup"><span data-stu-id="536e3-104">DataFormats</span></span>

<span data-ttu-id="536e3-105">Especifica os formatos de dados padrão e principal com suporte por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="536e3-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="536e3-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="536e3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="536e3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="536e3-107">Remarks</span></span>

<span data-ttu-id="536e3-108">O valor de *arquivo/formato* especifica o arquivo principal padrão ou o formato de objeto para objetos dessa classe.</span><span class="sxs-lookup"><span data-stu-id="536e3-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="536e3-109">O valor de *formatos* especifica uma lista de formatos para implementações padrão de [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), em que *n* é um índice de inteiro baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="536e3-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="536e3-110">Por exemplo, *n*  =  *Format*, *Aspect*, *Medium*, *Flag*, em que *Format* é um formato de área de transferência, *Aspect* é um ou mais membros de [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* é um ou mais membros de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)e *Flag* é um ou mais membros de [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir).</span><span class="sxs-lookup"><span data-stu-id="536e3-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="536e3-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="536e3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="536e3-112">**IDataObject:: EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="536e3-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="536e3-113">**IDataObject:: GetData**</span><span class="sxs-lookup"><span data-stu-id="536e3-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="536e3-114">**IDataObject:: SetData**</span><span class="sxs-lookup"><span data-stu-id="536e3-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




