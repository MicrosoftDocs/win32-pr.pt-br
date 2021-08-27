---
description: Retorna uma matriz de provedores de protocolo de protocolo de protocolo SSL instalado (SSL).
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Função SslEnumProtocolProviders (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c0e20bd98f8f3e76d4185cf2a3aa52985d73f66ff1ea61ed50bf67552330290d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906678"
---
# <a name="sslenumprotocolproviders-function"></a>Função SslEnumProtocolProviders

A função **SslEnumProtocolProviders** retorna uma matriz de provedores de protocolo de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL) instalados.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwProviderCount* \[ fora\]
</dt> <dd>

Um ponteiro para um valor **DWORD** para receber o número de provedores de protocolo retornado.

</dd> <dt>

*ppProviderList* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe a matriz de estruturas [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt> </dl>         | O parâmetro *dwFlags* não é zero.<br/>                              |
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/>     |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *pdwProviderCount* ou *ppProviderList* é **nulo**.<br/> |



 

## <a name="remarks"></a>Comentários

Quando você terminar de usar a matriz de estruturas [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , chame a função [**SslFreeBuffer**](sslfreebuffer.md) para liberar a matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

