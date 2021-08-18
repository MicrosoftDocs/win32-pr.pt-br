---
description: Especifica o endereço do nó (Nad) a ser usado com a interface ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: Método ISCardCmd::p ut_Nad (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 84ade2e2ca69c328650f4c7df485814e4eaacedf3fdb0190fc883cde864a8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481386"
---
# <a name="iscardcmdput_nad-method"></a>Método Nad ISCardCmd::p ut \_

\[O **método \_ put Nad** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ put Nad** especifica o endereço do nó (Nad) a ser usado com a interface [**ISCardCmd.**](iscardcmd.md) Isso se aplica somente às comunicações usando o protocolo [*T=1.*](../secgloss/t-gly.md) Por padrão, o [**objeto ISCardCmd**](iscardcmd.md) usa um Nad de zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bNad* \[ Em\]
</dt> <dd>

Byte que representa o Nad a ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi concluída com êxito.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro bNad* não é válido.<br/>    |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado somente quando for necessário usar um valor diferente de zero para o Nad.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como especificar um endereço de nó a ser usado com a interface [**ISCardCmd.**](iscardcmd.md) O exemplo supõe que byNadValue é uma variável do tipo **BYTE** que foi atribuído anteriormente a um valor e que pISCardCmd é um ponteiro válido para uma instância da interface **ISCardCmd.**


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
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
</dt> </dl>

 

 
