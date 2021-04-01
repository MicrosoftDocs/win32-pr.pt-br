---
description: A função SelectNPPBlobFromTable seleciona uma NIC de uma tabela de BLOB NPP fornecida.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Função SelectNPPBlobFromTable (Netmon. h)
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
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164635"
---
# <a name="selectnppblobfromtable-function"></a>Função SelectNPPBlobFromTable

A função **SelectNPPBlobFromTable** seleciona uma NIC de uma tabela de blob NPP fornecida.

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

*HWND* \[ no\]
</dt> <dd>

Identificador para a janela que exibe a caixa de diálogo **selecionar uma rede** .

</dd> <dt>

*pBlobTable* \[ no\]
</dt> <dd>

Ponteiro para a tabela de BLOB fornecida. Monitor de Rede usa essa tabela para preencher a caixa de diálogo **selecionar uma rede** .

</dd> <dt>

*hBlob* \[ fora\]
</dt> <dd>

Identificador para o BLOB que representa a NIC selecionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida e o usuário selecionar uma NIC, o valor de retorno será NMERR \_ Success; o blob apontado por *hBlob* será preenchido.

Se o usuário não selecionar uma NIC, o valor de retorno será NMERR \_ nenhum \_ NPP \_ selecionado.

Se a função não for bem-sucedida, o valor de retorno será outro valor de NMERR.

## <a name="remarks"></a>Comentários

Quando chamado, Monitor de Rede exibe a caixa de diálogo **selecionar uma rede** , que pode ser usada para selecionar uma NIC. O BLOB NPP que representa a NIC selecionada retorna para o aplicativo de chamada.

Para aprender as várias maneiras que você pode selecionar NICs, consulte [selecionando uma placa de interface de rede](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Entradas de BLOB especiais](special-blob-entries.md)
</dt> </dl>

 

 




