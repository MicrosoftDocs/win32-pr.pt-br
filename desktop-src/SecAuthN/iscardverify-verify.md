---
description: Solicita uma verificação do usuário.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Método ISCardVerify:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751820"
---
# <a name="iscardverifyverify-method"></a>Método ISCardVerify:: Verify

\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Verify** solicita uma verificação do usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pcode* \[ no\]
</dt> <dd>

Contém o código a ser apresentado ao [*cartão inteligente*](../secgloss/s-gly.md) no processo de CHV (verificação de titular de cartão).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Indica se o código é global ou local.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ fl \_ IHV \_ global**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ fl \_ IHV \_ local**
</dt> </dl> </dd> <dt>

*lRef* \[ no\]
</dt> <dd>

Referência específica do cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método **Verify** retorna um dos seguintes valores:



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardVerify**](iscardverify.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
