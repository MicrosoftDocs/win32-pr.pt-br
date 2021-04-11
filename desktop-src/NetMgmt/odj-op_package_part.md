---
title: OP_PACKAGE_PART
description: Definição de IDL de OP_PACKAGE_PART
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104162953"
---
# <a name="op_package_part-structure"></a>Estrutura de OP_PACKAGE_PART

Define uma estrutura que contém um conjunto de dados identificado por um GUID.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Membros

### <a name="parttype"></a>Parte

Identifica a estrutura serializada contida em parte de acordo com a tabela a seguir:

|Parte|Significado|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|Contém uma estrutura de ODJ_WIN7_BLOB serializada.|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|Contém uma estrutura de OP_JOIN_PROV2_PART serializada.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Contém uma estrutura de OP_JOIN_PROV3_PART serializada.|
|GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}|Contém uma estrutura de OP_CERT_PART serializada.|
|GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}|Contém uma estrutura de OP_POLICY_PART serializada.|

### <a name="ulflags"></a>ulFlags

Deve ser definido como zero ou mais dos seguintes sinalizadores:

|Valor|Significado|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Essa parte do pacote é considerada essencial. Se o consumidor não reconhecer essa parte do pacote ou não conseguir processá-la com êxito, a operação geral deverá falhar.|

### <a name="part"></a>Parte

Contém uma estrutura serializada em uma estrutura de OP_BLOB. A estrutura específica é determinada por partType.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve ser definido como todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**BLOB de OP \_**](odj-op_blob.md)
