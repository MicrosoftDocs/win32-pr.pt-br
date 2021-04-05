---
title: Função MirrorIcon
description: Inverte os ícones (espelhos) para que sejam exibidos corretamente em um contexto de dispositivo espelhado.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Controles do Windows da função MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008997"
---
# <a name="mirroricon-function"></a>Função MirrorIcon

\[O **MirrorIcon** está disponível por meio do Windows XP com Service Pack 2 (SP2). Ele pode ser alterado ou indisponível nas versões subsequentes.\]

Inverte os ícones (espelhos) para que sejam exibidos corretamente em um contexto de dispositivo espelhado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phIconSmall* \[ entrada, saída, opcional\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Um ponteiro para o identificador de ícone que faz referência a uma pequena versão de um ícone.

</dd> <dt>

_phIconLarge * \[ in, out, opcional\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Um ponteiro para o identificador de ícone que faz referência a uma grande versão de um ícone.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**Verdadeiro se for** bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

**MirrorIcon** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 414 de ComCtl32.dll para obter um ponteiro de função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,81 ou posterior)</dt> </dl> |



 

