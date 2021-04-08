---
description: Seleciona uma NIC de registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Função GetNPPBlobFromUI (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922004"
---
# <a name="getnppblobfromui-function"></a>Função GetNPPBlobFromUI

A função **GetNPPBlobFromUI** seleciona uma NIC de registro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para uma janela que exibe a caixa de diálogo **selecionar uma rede** .

</dd> <dt>

*hFilterBlob* \[ no\]
</dt> <dd>

Um identificador para um [*blob de filtro*](f.md) usado para limitar quais NICs são exibidos.

</dd> <dt>

*phBlob* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador do BLOB que representa a NIC selecionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (o usuário seleciona uma NIC), o valor de retorno será NMERR com \_ êxito e o blob ao qual *phBlob* aponta será preenchido.

Se o usuário não selecionar uma NIC, o valor de retorno será **NMERR \_ nenhum \_ NPP \_ selecionado**.

Se a função não for bem-sucedida, o valor de retorno será outro valor de NMERR.

## <a name="remarks"></a>Comentários

Quando chamado, Monitor de Rede exibe a caixa de diálogo **selecionar uma rede** , que pode ser usada para selecionar uma NIC. O BLOB NPP que representa a NIC é retornado para o aplicativo de chamada.

Se o BLOB nomeado por *hFilterBlob* for um [*blob especial*](s.md), o localizador tentará processá-lo. Um exemplo seria uma chamada que anteriormente retornava um BLOB especial do NPP remoto. O aplicativo inseriu a marca necessária, \_ nome do computador. Nessa situação, o localizador passaria esse BLOB para o NPP remoto, que retornaria uma tabela de BLOBs NPP que representa o computador solicitado. Esses BLOBs de NPP remotos seriam exibidos na caixa de diálogo.

O chamador deve chamar a função [DestroyBlob](destroyblob.md) , que destrói o blob retornado quando ele não é mais necessário.



| Para saber mais sobre | Consulte                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Três maneiras de selecionar NICs  | [Selecionando uma placa de interface de rede](selecting-a-network-interface-card.md) |
| Especificando um BLOB de filtro   | [Especificando um BLOB de filtro](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




