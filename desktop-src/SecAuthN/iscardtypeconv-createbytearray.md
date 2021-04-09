---
description: Cria uma matriz de bytes C/C++ típica.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'Método ISCardTypeConv:: CreateByteArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091660"
---
# <a name="iscardtypeconvcreatebytearray-method"></a>Método ISCardTypeConv:: CreateByteArray

\[O método **CreateByteArray** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **CreateByteArray** cria uma matriz de bytes C/C++ típica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwAllocSize* \[ no\]
</dt> <dd>

Tamanho (em bytes) da memória a ser alocada para a matriz.

</dd> <dt>

*ppbyArray* \[ fora\]
</dt> <dd>

Ponteiro para a matriz de bytes a ser retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Para criar um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)), chame [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).

Para criar um SAFEARRAY de automação de caracteres não assinados (bytes), chame [**createsafearray**](iscardtypeconv-createsafearray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores de retorno do cartão inteligente](authentication-return-values.md)
</dt> <dt>

[**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[**Createsafearray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
