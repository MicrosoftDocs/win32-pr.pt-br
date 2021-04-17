---
description: Formata os dados da instância de propriedade usando o formatador genérico que o Monitor de Rede fornece.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Função FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790016"
---
# <a name="formatpropertyinstance-function"></a>Função FormatPropertyInstance

A função **FormatPropertyInstance** formata os dados da instância de propriedade usando o formatador genérico que o monitor de rede fornece.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpPropertyInst* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [PROPERTYINST](propertyinst.md) que contém os dados da instância.

Na entrada, o formatador genérico usa os dados da instância de um dos membros da União **PROPERTYINST** e converte esses dados em uma cadeia de caracteres formatada predefinida.

Na saída, o formatador genérico define o membro **szPropertyText** da estrutura **PROPERTYINST** como um ponteiro para a cadeia de caracteres formatada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro de NMerr. h.

## <a name="remarks"></a>Comentários

A DLL do analisador indiretamente chama a função **FormatPropertyInstance** quando o formatador genérico é necessário para formatar dados para exibição no painel de detalhes da interface do usuário do monitor de rede. Para chamar **FormatPropertyInstance** , especifique-o no membro **InstanceData** da estrutura [PROPERTYINFO](propertyinfo.md) quando você define a propriedade.

> [!Note]  
> O analisador não reconhece qual função é chamada quando deve formatar uma instância de uma propriedade. A função pode ser **FormatPropertyInstance** ou uma função de formato personalizada definida pelo analisador. O analisador chama qualquer função de formato especificada pelo membro **InstanceData** da estrutura **PROPERTYINFO** para a propriedade.

 

Para obter mais informações e um exemplo de como implementar [formatproperties](formatproperties.md), consulte [Implementing formatproperties](implementing-formatproperties.md). Para obter mais informações sobre como o formatador genérico formata diferentes tipos de dados, consulte [saída de formatador genérico](generic-formatter-output.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




