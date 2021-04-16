---
description: Configura o especialista no DLL especialista.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurar função de retorno de chamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758296"
---
# <a name="configure-callback-function"></a>Configurar função de retorno de chamada

A função **Configurar** configura o especialista na DLL do especialista.

O especialista deve implementar a função **Configurar** . Quando a chamada de função é recebida, o especialista exibe uma caixa de diálogo que permite ao usuário alterar qualquer item configurável.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador de especialista exclusivo.

O identificador exclusivo é passado de volta em todas as funções de Monitor de Rede específicas do especialista. Lembre-se de que o identificador pode não ser a mesma chave de especialista que foi passada para a função de [**execução**](run.md) . Não armazene a chave de especialista da chamada de **configuração** .

</dd> <dt>

*ppConfig* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**EXPERTCONFIG**](expertconfig.md) na entrada.

Após uma saída bem-sucedida, a estrutura [**EXPERTCONFIG**](expertconfig.md) referenciada contém os novos dados de configuração.

</dd> <dt>

*pExpertStartupInfo* \[ no\]
</dt> <dd>

Um ponteiro para o elemento capture com foco quando o especialista foi iniciado.

</dd> <dt>

*StartupFlags* \[ no\]
</dt> <dd>

Os sinalizadores que indicam como o especialista deve usar o parâmetro *pExpertStartupInfo* . O único sinalizador definido é um **sinalizador de inicialização de especialista que \_ \_ \_ usa dados de \_ inicialização \_ \_ em \_ \_ dados de configuração**. O sinalizador indica que o especialista usará o parâmetro *pExpertStartupInfo* em vez do parâmetro *ppConfig* que passou. Normalmente, você define o sinalizador ao iniciar o especialista em um menu de contexto.

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela pai. Use a alça para abrir uma caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se existir uma configuração atual), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Monitor de Rede chama a função **Configurar** com a configuração atual do especialista, se houver. O especialista exibe uma caixa de diálogo, com a qual você pode alterar qualquer item configurável.

Quando *ppConfig* é passado e monitor de rede não tem uma configuração armazenada para o especialista especificado, o valor do parâmetro pode ser **nulo**. Nesse caso, a função **Configure** pressupõe valores padrão embutidos em código (ou usa as informações de inicialização) para abrir a caixa de diálogo.

Os dados de configuração também podem ser **nulos** quando a função **Configure** retorna, e um **NULL** foi passado. Essa situação ocorre quando Monitor de Rede não tem um padrão armazenado e o usuário pressiona **Cancelar**.

O início da estrutura de dados [**EXPERTCONFIG**](expertconfig.md) inclui uma seção privada que armazena as informações de tamanho da estrutura. O tamanho da estrutura **EXPERTCONFIG** deve incluir o comprimento de **DWORD** reservado que aparece no início da estrutura. Por exemplo, se os dados de configuração exigirem 20 bytes de espaço de armazenamento, aloque 24 bytes para armazenar os dados. Se um *ppConfig* for **nulo**, a função **Configure** chamará a função [**ExpertAllocMemory**](expertallocmemory.md) para alocar uma nova configuração com o tamanho correto. Se o buffer não for suficiente para manter os dados de especialista, o especialista deverá chamar a função [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




