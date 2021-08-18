---
description: Incrementa a contagem de referência para uma instância protocolo SSL provedor SSL.
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Função SslIncrementProviderReferenceCount (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: a177d4142d304834aea773e56a09703bc4d56e6b479a2f005f00e3b692980c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905995"
---
# <a name="sslincrementproviderreferencecount-function"></a>Função SslIncrementProviderReferenceCount

A **função SslIncrementProviderReferenceCount** incrementa a contagem de referência para [*uma instância do*](/windows/desktop/SecGloss/s-gly) provedor SSL (protocolo protocolo SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ Em\]
</dt> <dd>

O handle para a instância do provedor de protocolo SSL.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                    | Descrição                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | O *alça hSslProvider* não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

