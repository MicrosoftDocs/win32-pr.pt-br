---
title: Função RasAdminFreeBuffer (Rassapi. h)
description: A função RasAdminFreeBuffer libera a memória que foi alocada pelo RAS em nome do chamador.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- Função RasAdminFreeBuffer RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757739"
---
# <a name="rasadminfreebuffer-function"></a>Função RasAdminFreeBuffer

\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0. Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]

A função **RasAdminFreeBuffer** libera a memória que foi alocada pelo RAS em nome do chamador.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ponteiro* \[ do no\]
</dt> <dd>

Ponteiro para o buffer a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.



| Valor                                                                                                    | Significado                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl> | O parâmetro de *ponteiro* é inválido.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Use a função **RasAdminFreeBuffer** para liberar os buffers alocados pelas funções [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/> | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funções de administração do servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

