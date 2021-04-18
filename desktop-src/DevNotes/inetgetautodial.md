---
description: A função InetGetAutodial retorna as configurações de discagem automática do registro.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Função InetGetAutodial
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756326"
---
# <a name="inetgetautodial-function"></a>Função InetGetAutodial

\[Essa função não tem suporte e pode ser alterada ou indisponível em versões futuras do Windows. \]

A função **InetGetAutodial** retorna as configurações de discagem automática do registro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpfEnable* \[ fora\]
</dt> <dd>

Indica se a AutoDiscagem está habilitada. Um valor **true** no retorno indica que A discagem automática está habilitada.

</dd> <dt>

*lpszEntryName* \[ fora\]
</dt> <dd>

No retorno, contém o nome da entrada do catálogo telefônico que está definida para a discagem automática.

</dd> <dt>

*cbEntryNameSize* \[ no\]
</dt> <dd>

Tamanho do buffer alocado pelo chamador para o nome de entrada do catálogo telefônico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                                | Descrição                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**êxito do erro \_**</dt> </dl>              | A chamada foi bem-sucedida.<br/>                                                                                                                       |
| <dl> <dt>**ERROS de \_ argumentos inválidos \_**</dt> </dl>       | *lpfEnable* ou *lpszEntryName* contém um ponteiro **nulo** ou o valor de *cbEntryNameSize* é zero.<br/>                                         |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>  | Memória insuficiente para alocar buffers internos.<br/>                                                                                    |
| <dl> <dt>**ERRO \_ de \_ buffer insuficiente**</dt> </dl> | *cbEntryNameSize* não indica que o buffer apontado por *lpszEntryName* é grande o suficiente para receber o nome da entrada do catálogo telefônico.<br/> |



 

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
