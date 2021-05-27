---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 3ba1b8f6e09212c1ba2f4a0093e2205acaa2e835
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548931"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>Função DWriteCoreCreateFactory (dwrite_core. h)

Cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.

> [!IMPORTANT]
> Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma. Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](../dwritecore-overview.md).

## <a name="syntax"></a>Sintaxe
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Parâmetros

`factoryType`

Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Um valor que especifica se o objeto de fábrica será compartilhado, isolado ou restrito.

`iid`

Tipo: <b>REFIID</b>

Um valor de GUID que identifica a interface de fábrica DirectWrite, como __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

`factory`

Tipo: <b>IUnknown * *</b>

Um endereço de um ponteiro para o objeto da fábrica DirectWrite recém-criado.

## <a name="return-value"></a>Retornar valor

Tipo: <b>HRESULT</b>

Se esse método tiver sucesso, ele retornará <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Caso contrário, ele retorna um código de erro <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Exemplos

Consulte o tópico [visão geral do DWriteCore](../dwritecore-overview.md) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Comentários

Isso é funcionalmente o mesmo que a função [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite. A função DWriteCore tem um nome diferente para evitar ambigüidade.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, reunião do projeto [aplicativos Win32] |
| **Cabeçalho** | dwrite. h (incluir dwrite_core. h) |