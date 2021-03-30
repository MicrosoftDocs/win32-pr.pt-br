---
title: IFillLockBytes-implementação
description: O sistema fornece uma implementação de IFillLockBytes como parte da implementação dos arquivos compostos.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implementação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916241"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes-implementação

O sistema fornece uma implementação de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) como parte da implementação dos arquivos compostos.

O download do código pode criar uma instância de um objeto de arquivo composto assíncrono chamando [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes). O download do código também pode criar uma instância de um objeto wrapper de matriz de bytes assíncronos em um arquivo ou matriz de bytes existente chamando a função [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) ou a função [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .

## <a name="when-to-use"></a>Quando usar

Atualmente, os monikers de URL são os únicos usuários da implementação de armazenamento assíncrono COM.

## <a name="remarks"></a>Comentários

A seguir estão os quatro métodos da implementação de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Grava um novo bloco de bytes no final de uma matriz de bytes. O tamanho do bloco é especificado como um parâmetro para [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Grava um novo bloco de dados em um local especificado na matriz de bytes.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes:: preenche**
</dt> <dd>

Define o tamanho da matriz de bytes. Retorna E \_ falha de chamadas para [**ILockBytes:: ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) que tentam acessar dados além do limite superior especificado pelo método.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes:: Terminate**
</dt> <dd>

Informa a matriz de bytes que um download foi encerrado, com êxito ou sem êxito.

</dd> </dl>

 

 




