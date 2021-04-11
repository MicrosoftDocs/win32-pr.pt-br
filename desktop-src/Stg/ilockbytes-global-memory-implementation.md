---
title: ILockBytes-implementação de memória global
description: A implementação de memória global ILockBytes é implementada em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e projetada para leitura e gravação diretamente na memória global.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implementações, memória global
- ILockBytes Strctd STG, implementações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291905"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes-implementação de memória global

A implementação de memória global ILockBytes é implementada em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e projetada para leitura e gravação diretamente na memória global.

## <a name="when-to-use"></a>Quando usar

Os métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) são chamados das implementações de arquivo composto de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no objeto de armazenamento de arquivo composto criado por meio de uma chamada para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).

## <a name="remarks"></a>Comentários

A seguir estão os métodos da implementação de memória global [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**
</dt> <dd>

Lê um bloco de bytes de um deslocamento especificado no início da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**
</dt> <dd>

Grava o bloco de bytes de um deslocamento especificado no início da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: flush**
</dt> <dd>

Diferentemente da implementação baseada em arquivo, chamar esse método na implementação de memória global não tem nenhum efeito.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Define o tamanho da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Essa implementação não dá suporte ao bloqueio, portanto *dwLocksType* está definido como zero. O chamador deve garantir que os acessos sejam válidos e mutuamente exclusivos.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Esta implementação não dá suporte a bloqueio.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

A implementação de [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornecida pelo com chama o método [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar dados sobre o objeto da matriz de bytes. Se não houver nenhum nome razoável para a matriz de bytes, o método **ILockBytes:: stat** fornecido com retornará **NULL** no membro **pwcsName** da estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




