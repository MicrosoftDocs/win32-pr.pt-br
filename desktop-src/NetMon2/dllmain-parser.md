---
description: A função de exportação DllMain para o analisador identifica a existência do analisador e libera os recursos que Monitor de Rede usa para o analisador. DllMain deve ser implementado em todas as DLLs do analisador.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Função de retorno de chamada do DllMain Parser (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783260"
---
# <a name="dllmain-parser-callback-function"></a>Função de retorno de chamada de análise DllMain

A função de exportação **DllMain** para o analisador identifica a existência do analisador e libera os recursos que monitor de rede usa para o analisador. **DllMain** deve ser implementado em todas as DLLs do analisador.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HINSTANCE* \[ no\]
</dt> <dd>

Identificador para uma instância do analisador.

</dd> <dt>

*Comando* \[ no\]
</dt> <dd>

Indicador para determinar por que a função é chamada. Para obter uma lista de todos os sinalizadores possíveis, consulte [DllMain](/windows/desktop/Dlls/dllmain). A implementação do analisador deve processar os valores a seguir.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**\_anexar processo de dll \_**</dt> </dl> | Quando **DllMain** é chamado pela primeira vez, a DLL deve chamar [createprotocol](createprotocol.md) para fornecer informações a monitor de rede. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**desanexar processo de DLL \_ \_**</dt> </dl> | Quando **DllMain** é chamado pela última vez, a DLL deve chamar [DestroyProtocol](destroyprotocol.md) para liberar os recursos que a dll usa. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Não usado agora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A DLL do analisador sempre retorna **true**.

## <a name="remarks"></a>Comentários

O sistema operacional chama **DllMain** para carregar e descarregar a DLL do analisador. Essa função é baseada na função [DllMain](/windows/desktop/Dlls/dllmain) da biblioteca de vínculo dinâmico.

Você também pode usar a implementação de **DllMain** para armazenar uma instância de um analisador para uso no futuro. Por exemplo, você pode armazenar uma instância de DLL do parser e usá-la para uma chamada do sistema no futuro.



| Para obter informações sobre                                        | Consulte                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                  |
| Quais pontos de entrada são incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md)  |
| A implementação de **DllMain**  inclui um exemplo.        | [Implementando DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Createprotocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

