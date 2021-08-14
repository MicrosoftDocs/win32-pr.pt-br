---
title: Dataformats
description: Especifica os formatos de dados padrão e principal com suporte por um aplicativo.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Chave do Registro dataFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310594"
---
# <a name="dataformats"></a>Dataformats

Especifica os formatos de dados padrão e principal com suporte por um aplicativo.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Comentários

O *valor de arquivo/formato* especifica o arquivo principal padrão ou o formato de objeto para objetos dessa classe.

O *valor formats* especifica uma lista de formatos para implementações padrão de [**EnumFormatEtc,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)em que *n* é um índice inteiro baseado em zero. Por exemplo, *n* formato , aspecto , médio , sinalizador , em que format é um formato de área de transferência, o aspecto é um ou mais membros de  =    [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect),    *medium*  é um ou mais membros [**do TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)e o sinalizador é um ou mais membros de [**DATADIR.**](/windows/win32/api/objidl/ne-objidl-datadir) 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




