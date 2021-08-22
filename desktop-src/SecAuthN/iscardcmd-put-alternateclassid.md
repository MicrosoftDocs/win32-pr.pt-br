---
description: Especifica um novo identificador de classe alternativo na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: Método ISCardCmd::p ut_AlternateClassId (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fd1f74dee017cb72a67ecb4a9fc42da85153966336b25e54819be13464b3b7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481556"
---
# <a name="iscardcmdput_alternateclassid-method"></a>Método AlternateClassId ISCardCmd::p ut \_

\[O **método \_ alternateClassId** put está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ alternateClassId** put especifica um novo identificador de classe alternativo na APDU (unidade de dados [*do*](../secgloss/a-gly.md) protocolo de aplicativo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byClass* \[ Em\]
</dt> <dd>

Identificador de classe alternativo. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro byClass* não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

Com as comunicações usando o protocolo [*T=0*](../secgloss/t-gly.md), comandos de cartão adicionais podem ser gerados automaticamente pelo APDU e enviados para a TPDU (unidade de dados do protocolo de transmissão). Os comandos adicionais normalmente usam a mesma ID de classe que o comando original; especificar uma nova ID de classe por meio desse método permite que comandos gerados automaticamente usem a nova ID de classe.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir um novo identificador de classe alternativo na APDU (unidade de dados do protocolo [*de*](../secgloss/a-gly.md) aplicativo). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd.**](iscardcmd.md)


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd é definido como \_ D5778AE3-43DE-11D0-9171-00AAA00C18068<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**get \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
