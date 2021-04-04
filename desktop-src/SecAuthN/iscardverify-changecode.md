---
description: Substitui o código atual de CHV (verificação de titular de cartão) por um novo código CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Método ISCardVerify:: ChangeCode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662328"
---
# <a name="iscardverifychangecode-method"></a>Método ISCardVerify:: ChangeCode

\[O método **ChangeCode** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ChangeCode** substitui o código de CHV atual (verificação de titular de cartão) pelo novo código CHV.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOldCode* \[ no\]
</dt> <dd>

Ponteiro para um [**IByteBuffer**](ibytebuffer.md) que contém o código atual do usuário.

</dd> <dt>

*pNewCode* \[ no\]
</dt> <dd>

Ponteiro para um [**IByteBuffer**](ibytebuffer.md) que contém o novo código que será apresentado ao [*cartão inteligente*](../secgloss/s-gly.md) durante o processo de alteração para autenticar o usuário.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Indica se o código é global ou local e se o código deve ser habilitado ou desabilitado.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ fl \_ IHV \_ global**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ fl \_ IHV \_ local**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**\_habilitar SC FL \_ IHV \_**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**\_desabilitar o \_ IHV \_ fl do SC**
</dt> </dl> </dd> <dt>

*lRef* \[ no\]
</dt> <dd>

Referência específica do cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



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

[**IByteBuffer**](ibytebuffer.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[Valores de retorno do cartão inteligente](authentication-return-values.md)
</dt> </dl>

 

 
