---
description: A estrutura SESSIONSTATS fornece estatísticas sobre uma sessão.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Estrutura SESSIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 231c94d2abda40974249f6c3cc82c8efc7518cb21d5881f44e63f647bcb21de2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128826"
---
# <a name="sessionstats-structure"></a>Estrutura SESSIONSTATS

A estrutura **SESSIONSTATS** fornece estatísticas sobre uma [*sessão*](s.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**NextSession**
</dt> <dd>

Índice da próxima sessão do proprietário da estação.

</dd> <dt>

**StationOwner**
</dt> <dd>

Índice de uma estação proprietária dentro da matriz de estrutura [STATIONSTATS](stationstats.md) associada. A estação do proprietário é a estação que iniciou a sessão, a estação que enviou os pacotes da sessão.

</dd> <dt>

**StationPartner**
</dt> <dd>

Índice da outra estação dentro da matriz de estrutura [STATIONSTATS](stationstats.md) associada. A estação de parceiro é a estação que recebeu os pacotes da sessão.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

Número de pacotes enviados na sessão.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Monitor de Rede armazena informações de sessão e de estação em duas matrizes associadas, cujos elementos são estruturas **SESSIONSTATS** e [STATIONSTATS](stationstats.md) , respectivamente. Os membros dessas estruturas podem ser usados para navegar entre eles. Por exemplo, para mover para a próxima sessão para um proprietário de estação específico, use **NextSession**. Para saltar para o proprietário e a estação de parceiro da sessão na matriz STATIONSTATS, use o índice fornecido em **StationOwner** e **StationPartner**.

> [!Note]  
> A matriz SESSIONSTATS contém um elemento para cada sessão na captura atual. O algoritmo Monitor de Rede usado para adicionar elementos à matriz SESSIONSTATS baseia-se em informações de gravação eficiente enquanto a captura está em andamento. Consequentemente, a próxima sessão para uma estação de proprietário específica nem sempre é o próximo elemento na matriz.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




