---
title: IFillLockBytes – Implementação
description: O sistema fornece uma implementação de IFillLockBytes como parte da implementação de Arquivos Compostos.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd Stg , implementação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663016"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes – Implementação

O sistema fornece uma [**implementação de IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) como parte da implementação de Arquivos Compostos.

Baixar o código pode criar uma instância de um objeto de Arquivo Composto assíncrono chamando [**StgOpenAsyncDocFileOnIFillLockBytes.**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes) Baixar código também pode criar uma instância de um objeto wrapper de matriz de byte assíncrono em um arquivo existente ou matriz de byte chamando a [**função StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) ou a [**função StgGetIFillLockBytesOnILockBytes.**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)

## <a name="when-to-use"></a>Quando usar

Atualmente, os monikers de URL são os únicos usuários da implementação de armazenamento assíncrono COM.

## <a name="remarks"></a>Comentários

A seguir estão os quatro métodos da implementação [**IFillLockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Grava um novo bloco de bytes no final de uma matriz de bytes. O tamanho do bloco é especificado como um parâmetro para [**FillAppend.**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Grava um novo bloco de dados em um local especificado na matriz de byte.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

Define o tamanho da matriz de byte. Retorna E \_ FAIL de chamadas para [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) que tentam acessar dados além do limite superior especificado pelo método .

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**
</dt> <dd>

Informa à matriz de byte que um download foi encerrado, com êxito ou sem êxito.

</dd> </dl>

 

 




