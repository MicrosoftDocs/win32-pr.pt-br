---
description: Define o campo de dados na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd: método de ut_Data de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090926"
---
# <a name="iscardcmdput_data-method"></a>Método de dados ISCardCmd::p UT \_

\[O método **Put \_ Data** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Put \_ Data** define o campo de dados na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ no\]
</dt> <dd>

Ponteiro para o **IStream**(objeto de buffer de bytes) a ser copiado para o campo de dados APDU.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pData* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pData*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                       |



 

## <a name="remarks"></a>Comentários

Quando você define uma nova parte de dados da mensagem, o comprimento do campo de dados é calculado e armazenado no parâmetro P3 do APDU. Para recuperar o comprimento do campo de dados, chame [**Get \_ P3**](iscardcmd-get-p3.md).

Para recuperar o campo de dados do APDU, chame [**obter \_ dados**](iscardcmd-get-data.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir o campo de dados na [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU). O exemplo supõe que pIByteData é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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

[**obter \_ dados**](iscardcmd-get-data.md)
</dt> <dt>

[**obter \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
