---
description: O método Read lê um número especificado de bytes do objeto buffer na memória, começando no ponteiro de busca atual.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Método IByteBuffer:: Read (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482666"
---
# <a name="ibytebufferread-method"></a>Método IByteBuffer:: Read

\[O método **Read** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **Read** lê um número especificado de bytes do objeto buffer na memória, começando no ponteiro de busca atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pByte* \[ fora\]
</dt> <dd>

Aponta para o buffer no qual os dados de fluxo são lidos. Se ocorrer um erro, esse valor será **NULL**.

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Número de bytes de dados para tentar ler do objeto de fluxo.

</dd> <dt>

*pcbRead* \[ fora\]
</dt> <dd>

Endereço de uma variável **longa** que recebe o número real de bytes lidos do objeto de fluxo. Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor. Nesse caso, esse método não fornece o número real de bytes lidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método lê bytes deste objeto de fluxo na memória. O objeto de fluxo deve ser aberto no \_ modo de leitura STGM. Esse método ajusta o ponteiro de busca pelo número real de bytes lidos.

O número de bytes realmente lidos também é retornado no parâmetro *pcbRead* .

Notas aos Chamadores

O número real de bytes lidos pode ser menor que o número de bytes solicitados se ocorrer um erro ou se o final do fluxo for atingido durante a operação de leitura.

Algumas implementações podem retornar um erro se o final do fluxo for atingido durante a leitura. Você deve estar preparado para lidar com os valores de retorno de erro ou erros \_ de retorno em OK no fim das leituras de fluxo.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra os bytes de leitura do buffer.


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

