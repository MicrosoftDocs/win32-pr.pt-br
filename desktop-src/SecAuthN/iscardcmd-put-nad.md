---
description: Especifica o endereço do nó (NAD) a ser usado com a interface ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: método de ut_Nad de:p (Scarddat. h)'
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
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827462"
---
# <a name="iscardcmdput_nad-method"></a>Método ISCardCmd::p UT \_ nad

\[O método do **\_ nad Put** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método da **\_ nad Put** especifica o endereço do nó (NAD) a ser usado com a interface [**ISCardCmd**](iscardcmd.md) . Isso se aplica às comunicações usando apenas as comunicações de [*protocolo T = 1*](../secgloss/t-gly.md) . Por padrão, o objeto [**ISCardCmd**](iscardcmd.md) usa um nad de zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bNad* \[ no\]
</dt> <dd>

Byte que representa o NAD a ser usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi concluída com êxito.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *bNad* não é válido.<br/>    |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado somente quando for necessário usar um valor diferente de zero para o NAD.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como especificar um endereço de nó para usar com a interface [**ISCardCmd**](iscardcmd.md) . O exemplo supõe que byNadValue é uma variável do tipo **byte** que anteriormente atribuiu um valor e que pISCardCmd é um ponteiro válido para uma instância da interface **ISCardCmd** .


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
</dt> </dl>

 

 
