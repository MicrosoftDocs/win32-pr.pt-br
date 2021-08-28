---
description: A função de exportação de registro deve ser implementada em todas as DLLs do analisador. A implementação do registro cria e preenche um banco de dados de propriedade para um protocolo. Monitor de Rede usa o banco de dados para determinar a quais propriedades o protocolo dá suporte.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Registrar função de retorno de chamada do analisador (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 4c24f719018f155fab26df4673b7dc3be18546675532657cb8fb3a0271763af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128916"
---
# <a name="register-parser-callback-function"></a>Registrar função de retorno de chamada do analisador

A função de exportação de **registro** deve ser implementada em todas as DLLs do analisador. A implementação do **registro** cria e preenche um banco de [*dados de propriedade*](p.md) para um protocolo. Monitor de Rede usa o banco de dados para determinar a quais propriedades o protocolo dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

O identificador do protocolo que o Monitor de Rede fornece ao chamar **o registro**. O identificador *hProtocol* é necessário ao chamar funções auxiliares de exportação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum.

## <a name="remarks"></a>Comentários

Monitor de Rede começa a chamar a função de **registro** assim que uma captura é carregada. Monitor de Rede chama a função de **registro** para cada protocolo que pode identificar. A função [createprotocol](createprotocol.md) passa um ponteiro para a função **Register** .

A implementação do **registro** inclui chamadas para as funções a seguir.

-   Uma chamada para as funções [CreatePropertyDatabase](createpropertydatabase.md) e [AddProperty](/previous-versions/bb251873(v=msdn.10)) para criar um banco de dados de todas as propriedades às quais o protocolo dá suporte.
-   Uma chamada para a função [Createentregatable](createhandofftable.md) será necessária se o protocolo usar um [*conjunto de entrega*](h.md).

Se a DLL do analisador contiver vários analisadores e o analisador puder detectar mais de um protocolo, você deverá implementar uma função de **registro** para cada protocolo.



| Para obter informações sobre                                        | Consulte                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                 |
| Quais pontos de entrada são incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md) |
| Como implementar **o registro**  inclui um exemplo.       | [Implementando o registro](implementing-register.md)     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[Createentregatable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[Createprotocol](createprotocol.md)
</dt> </dl>

 

