---
title: Função GetProcessHandleFromHwnd
description: Recupera um identificador de processo de um identificador de janela.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Acessibilidade do Windows da função GetProcessHandleFromHwnd
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085602"
---
# <a name="getprocesshandlefromhwnd-function"></a>Função GetProcessHandleFromHwnd

Recupera um identificador de processo de um identificador de janela.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

O identificador da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **identificador**](/windows/desktop/WinProg/windows-data-types)**

Se for bem-sucedido, retorna o identificador do processo que possui a janela.

Se não for bem-sucedido, retornará **NULL**.

## <a name="remarks"></a>Comentários

Em versões anteriores do sistema operacional, um processo poderia abrir outro processo (para acessar sua memória, por exemplo) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Essa função terá sucesso se o chamador tiver os privilégios apropriados; Normalmente, o chamador e o processo de destino devem ser o mesmo usuário.

No Windows Vista, no entanto, o [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) falha no cenário em que o chamador tem o UIAccess e o processo de destino é elevado. Nesse caso, o proprietário do processo de destino está no grupo Administradores, mas o processo de chamada está sendo executado com o token restrito, portanto, não tem associação nesse grupo e tem acesso negado ao processo elevado. No entanto, se o chamador tiver o UIAccess, ele poderá usar um gancho do Windows para injetar código no processo de destino e, no processo de destino, enviar um identificador de volta para o chamador.

**GetProcessHandleFromHwnd** é uma função de conveniência que usa essa técnica para obter o identificador do processo que possui o HWND especificado. Observe que ele só é bem sucedido nos casos em que o chamador e o processo de destino estão sendo executados como o mesmo usuário. O identificador retornado tem os seguintes privilégios: processo de identificador de DUP processo operação de VM processar processo de leitura da VM \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ gravação \| sincronizar. Se outros privilégios forem necessários, talvez seja necessário implementar explicitamente a técnica de conexão em vez de usar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

