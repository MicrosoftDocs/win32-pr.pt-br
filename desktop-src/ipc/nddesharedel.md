---
description: Exclui um compartilhamento DDE do DSDM (Gerenciador de banco de dados de compartilhamento) DDE.
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Função NDdeShareDel (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760053"
---
# <a name="nddesharedel-function"></a>Função NDdeShareDel

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Exclui um compartilhamento DDE do DSDM (Gerenciador de banco de dados de compartilhamento) DDE.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento a ser excluído do DSDM. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*wReserved* \[ no\]
</dt> <dd>

Reservado. Esse parâmetro deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

Para excluir um compartilhamento DDE do DSDM, você deve ter o privilégio apropriado. O criador de compartilhamento tem o privilégio de exclusão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareDelW** (Unicode) e **NDdeShareDelA** (ANSI)<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> </dl>

 

 




