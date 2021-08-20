---
title: ILockBytes-implementação de File-Based
description: Implementado em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e criado para leitura e gravação diretamente em um arquivo de disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implementações, com base em arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3dcfd11562f6a023d1f77af44b51ff7016cb61afdb16f2e4d72f81114fc132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961805"
---
# <a name="ilockbytes---file-based-implementation"></a>ILockBytes-implementação de File-Based

Implementado em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e criado para leitura e gravação diretamente em um arquivo de disco.

## <a name="when-to-use"></a>Quando usar

Os métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) são chamados das implementações de arquivo composto de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no objeto de armazenamento de arquivo composto criado por meio de uma chamada para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), portanto, você não precisa chamá-los diretamente.

## <a name="remarks"></a>Comentários

A seguir estão os métodos da implementação de File-Based do [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**
</dt> <dd>

Lê um bloco de bytes de um deslocamento especificado no início da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**
</dt> <dd>

Grava um bloco de bytes de um deslocamento especificado no início da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: flush**
</dt> <dd>

Garante que todos os buffers internos mantidos pela implementação do [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sejam gravados no armazenamento físico subjacente.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Define o tamanho da matriz de bytes.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

O parâmetro *dwLockTypes* é definido para bloquear \_ ONLYONCE ou bloqueio \_ exclusivo, o que permitirá ou restringirá o acesso a regiões bloqueadas.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Esse método desbloqueia a região bloqueada por [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

A implementação de [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornecida pelo com chama o método [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar informações sobre o objeto da matriz de bytes. Se não houver nenhum nome razoável para a matriz de bytes, o método **ILockBytes:: stat** fornecido com retornará **NULL** no membro **pwcsName** da estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




