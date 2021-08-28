---
description: A função SelectNPPBlobFromTable seleciona uma NIC de uma tabela de BLOB NPP fornecida.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Função SelectNPPBlobFromTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14d9ca14d027efc1540f5a5d2ae78e948da68dd59247252989b617d07229bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074406"
---
# <a name="selectnppblobfromtable-function"></a>Função SelectNPPBlobFromTable

A **função SelectNPPBlobFromTable** seleciona uma NIC de uma tabela de BLOB NPP fornecida.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwnd* \[ Em\]
</dt> <dd>

Lidar com a janela que exibe a **caixa de diálogo Selecionar uma** rede.

</dd> <dt>

*pBlobTable* \[ Em\]
</dt> <dd>

Ponteiro para a tabela BLOB fornecida. Monitor de Rede usa essa tabela para preencher a **caixa de diálogo Selecionar uma** rede.

</dd> <dt>

*hBlob* \[ out\]
</dt> <dd>

Lidar com o BLOB que representa a NIC selecionada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida e o usuário selecionar uma NIC, o valor de retorno será NMERR SUCCESS; o BLOB apontado por \_ *hBlob* será preenchido.

Se o usuário não selecionar uma NIC, o valor de retorno será NMERR \_ NO \_ NPP \_ SELECTED.

Se a função não for bem-sucedida, o valor de retorno será outro valor NMERR.

## <a name="remarks"></a>Comentários

Quando chamado, Monitor de Rede exibe **a caixa** de diálogo Selecionar uma rede, que você pode usar para selecionar uma NIC. O BLOB NPP que representa a NIC selecionada retorna para o aplicativo de chamada.

Para saber as várias maneiras de selecionar NICs, consulte [Selecionar uma placa de interface de rede](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Entradas de BLOB especiais](special-blob-entries.md)
</dt> </dl>

 

 




