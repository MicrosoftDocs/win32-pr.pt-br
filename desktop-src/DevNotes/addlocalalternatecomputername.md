---
description: Adiciona um nome de rede local alternativo para o computador do qual ele é chamado.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Função AddLocalAlternateComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751558"
---
# <a name="addlocalalternatecomputername-function"></a>Função AddLocalAlternateComputerName

Adiciona um nome de rede local alternativo para o computador do qual ele é chamado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpDnsFQHostname* \[ no\]
</dt> <dd>

O nome alternativo a ser adicionado. O nome deve estar no formato **ComputerNameDnsFullyQualified** , conforme definido na enumeração [**de \_ \_ formato de nome do computador**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , e a função [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) deve ser capaz de validá-lo com seu formato definido como **DnsNameHostnameFull**.

</dd> <dt>

*ulFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará **\_ êxito de erro**. Se a função falhar, ela retornará um código de erro diferente de zero. Entre os códigos de erro que ele retorna estão os seguintes:



| Código de retorno                                                                                               | Descrição                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>  | Indica que o parâmetro *lpDnsFQHostname* não aponta para um nome DNS válido ou que o parâmetro *ulFlags* não é igual a zero.<br/> |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl> | Não há memória suficiente para concluir a operação.<br/>                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Biblioteca<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Nomes Unicode e ANSI<br/> | **AddLocalAlternateComputerNameW** (Unicode) e **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_formato do nome do computador \_**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
