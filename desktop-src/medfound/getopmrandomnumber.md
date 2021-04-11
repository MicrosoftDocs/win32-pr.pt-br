---
description: Obtém um número aleatório de 128 bits, criptograficamente seguro, de um objeto de saída protegido.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Função GetOPMRandomNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296139"
---
# <a name="getopmrandomnumber-function"></a>Função GetOPMRandomNumber

> [!IMPORTANT]
> Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Obtém um número aleatório de 128 bits, criptograficamente seguro, de um objeto de saída protegido.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opoOPMProtectedOutput* \[ no\]
</dt> <dd>

Um identificador para o objeto de saída protegido. Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*prnRandomNumber* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de **\_ \_ \_ número aleatório DXGKMDT OPM** que recebe o número aleatório.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções OPM](opm-functions.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 
