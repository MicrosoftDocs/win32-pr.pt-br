---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica o tipo de objeto de fábrica DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 85f74d72dc8799a7a3c78603ec0dd5f9c118fdb1
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954999"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>Enumeração de DWRITE_FACTORY_TYPE (DWRITE. h)

Especifica o tipo de objeto de fábrica DirectWrite.

> [!IMPORTANT]
> Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma. Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview).

## <a name="syntax"></a>Sintaxe
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>Constantes

| Nome | Descrição |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indica que a fábrica DirectWrite é uma fábrica compartilhada e que permite a reutilização de dados de fontes armazenados em cache em vários componentes em processo. Essas fábricas também aproveitam os componentes de cache de fonte de processo cruzado para melhorar o desempenho. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indica que o objeto de fábrica DirectWrite está isolado. Os objetos criados a partir da fábrica isolada não interagem com o estado interno do DirectWrite de outros componentes. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Indica que o objeto de fábrica DirectWrite é restrito. Os objetos criados a partir de uma fábrica restrita não usam nem modificam os dados de estado interno ou armazenados em cache usados por outras fábricas. Além disso, a coleção de fontes do sistema contém apenas fontes conhecidas.|

## <a name="examples"></a>Exemplos

Consulte o tópico [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Comentários

Um objeto de fábrica DirectWrite contém informações sobre seu estado interno, como registro de carregador de fonte e dados de fonte em cache. Na maioria dos casos, você deve usar o objeto de fábrica compartilhado, pois ele permite que vários componentes usem o DirectWrite para compartilhar informações de estado DirectWrite internas, reduzindo assim o uso de memória. No entanto, há casos em que é desejável reduzir o impacto de um componente no restante do processo, como um plug-in de uma fonte não confiável, na área restrita e no isolamento do restante dos componentes do processo. Nesses casos, você deve usar uma fábrica isolada para o componente de área restrita.

Uma fábrica restrita é mais bloqueada do que uma fábrica isolada. Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma. Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas. Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão de DWRITE mais antiga que DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) retornará **E_INVALIDARG**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, reunião do projeto [aplicativos Win32] |
| **Cabeçalho** | dwrite. h (incluir dwrite_core. h) |
