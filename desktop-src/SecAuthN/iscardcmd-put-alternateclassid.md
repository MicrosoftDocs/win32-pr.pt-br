---
description: Especifica um novo identificador de classe alternativo na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd: método de ut_AlternateClassId de:p (Scarddat. h)'
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
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747931"
---
# <a name="iscardcmdput_alternateclassid-method"></a>ISCardCmd: método UT \_ AlternateClassId:p

\[O método **Put \_ AlternateClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Put \_ AlternateClassId** especifica um novo identificador de classe alternativo na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byClass* \[ no\]
</dt> <dd>

Identificador de classe alternativo. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *byClass* não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

Com as comunicações usando o [*protocolo T = 0*](../secgloss/t-gly.md), comandos de cartão adicionais podem ser gerados automaticamente pelo APDU e enviados para a unidade de dados do protocolo de transmissão (TPDU). Os comandos adicionais normalmente usam a mesma ID de classe que o comando original; a especificação de uma nova ID de classe por meio desse método permite que comandos gerados automaticamente usem a nova ID de classe.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir um novo identificador de classe alternativo na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**obter \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
