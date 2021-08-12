---
description: Cria um objeto de contexto que descreve o dispositivo de tablet especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: Método ITablet::CreateContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 8b67e4c15d40f2da7a616295f10a7762b242fb40d9c0b5f42c00eb51d190cc03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450571"
---
# <a name="itabletcreatecontext-method"></a>Método ITablet::CreateContext

Cria um objeto de contexto que descreve o dispositivo de tablet especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWnd* \[ Em\]
</dt> <dd>

A janela à qual o contexto do tablet será anexado.

</dd> <dt>

*prcInput* \[ Em\]
</dt> <dd>

\[in, unique\]

O retângulo de entrada de tinta.

</dd> <dt>

*dwOptions* \[ Em\]
</dt> <dd>

Sinalizadores que configuram opções de contexto de tablet.

</dd> <dt>

*pTCS* \[ Em\]
</dt> <dd>

\[in, unique\]

Informações detalhadas sobre o contexto do tablet a ser criado.

</dd> <dt>

*cet* \[ Em\]
</dt> <dd>

Valor que habilita ou desabilita mensagens de contexto que estão sendo enviadas para a janela.

</dd> <dt>

*ppCtx* \[ out\]
</dt> <dd>

Um ponteiro para o contexto de tablet recém-criado.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Valor que identifica exclusivamente o tablet.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Ponteiro para informações sobre quais dados estão contidos em cada pacote.

</dd> <dt>

*pSink* \[ Em\]
</dt> <dd>

O [**objeto ITabletEventSink**](itableteventsink.md) para o qual as mensagens de notificação serão enviadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo obtém os valores padrão do Método [**ITablet::GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica os valores para atender às suas necessidades e, em seguida, passa a estrutura de configurações modificadas para o Método **ITablet::CreateContext**.

> [!Note]  
> Você deve implementar a [**Interface ITabletEventSink**](itableteventsink.md) ao chamar o **método ITablet::CreateContext**.

 

O *parâmetro dwOptions* é um conjunto de sinalizadores de bits que descrevem as opções de contexto. A tabela a seguir descreve esses sinalizadores.



| Nome do sinalizador                                | Valor                                                                                                                                                                                         | Descrição                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MARGEM DO \_ TCXO<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Especifica que o contexto de entrada no tablet terá uma margem. A margem é uma área fora da área de entrada especificada em que os eventos serão mapeados para a borda da área de entrada. Esse recurso facilita a entrada de pontos na borda do contexto.<br/> |
| TCXO \_ PREHOOK<br/>                 | 0x00000002<br/>                                                                                                                                                                         | O pré-hook obtém pacotes antes de contextos regulares e posthooks. Eles obterão pacotes na ordem de sua criação.<br/>                                                                                                                                                  |
| ESTADO DO CURSOR TCXO \_ \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | O TC retornará pacotes mesmo se o cursor estiver ativos. Por padrão, um TC só retornará pacotes quando o cursor estiver inoc baixo.<br/>                                                                                                                                       |
| TCXO \_ SEM \_ CURSOR PARA \_ BAIXO<br/>        | 0x00000008<br/>                                                                                                                                                                         | O TC não retornará pacotes quando o cursor estiver inoC.<br/>                                                                                                                                                                                                       |
| TCXO \_ NÃO \_ INTEGRADO<br/>         | 0x00000010<br/>                                                                                                                                                                         | O contexto não será integrado.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | Os posthooks obterão pacotes após contextos de tablet regulares, mas antes do contexto do sistema. Eles obterão pacotes na ordem inversa de sua criação.<br/>                                                                                                                   |
| TCXO \_ DONT \_ SHOW \_ CURSOR<br/>      | 0x00000080<br/>                                                                                                                                                                         | O TC não definirá a posição do cursor.<br/>                                                                                                                                                                                                                      |
| TCXO \_ NÃO \_ \_ VALIDAR TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | O TC não validará os GUIDS passados nas configurações de contexto do tablet em relação às propriedades com suporte do dispositivo.<br/>                                                                                                                                      |
| TCXO \_ PERMITIR \_ MOVIMENTO<br/>           | 0x00000400<br/>                                                                                                                                                                         | O TC permitirá que a detecção de movimento seja realizada (por padrão, isso só é permitido em contextos do sistema) e o cliente obterá ES \_ eventos DE MOVIMENTO.<br/>                                                                                                               |
| TCXO \_ PERMITIR \_ \_ TOQUES DE COMENTÁRIOS<br/>   | 0x00000800<br/>                                                                                                                                                                         | O TC permitirá que os comentários de caneta sejam mostrados. Por padrão, isso só é permitido em contextos do sistema.<br/>                                                                                                                                                              |
| TCXO \_ ALLOW \_ FEEDBACK \_ BARREL<br/> | 0x00001000<br/>                                                                                                                                                                         | O TC permitirá que os comentários de caneta sejam mostrados. Por padrão, isso só é permitido em contextos do sistema.<br/>                                                                                                                                                              |
| TCXO \_ ALL<br/>                     | TCXO \_ MARGIN \| TCXO \_ PREHOOK \| TCXO \_ CURSOR \_ STATE \| TCXO \_ NO \_ CURSOR \_ DOWN \| TCXO \_ NON \_ INTEGRATED \| TCXO \_ POSTHOOK \| TCXO \_ DONT \_ SHOW \_ CURSOR \| TCXO \_ DONT \_ VALIDATE \_ TCS<br/> | Todas as opções de contexto de tablet definidas.<br/>                                                                                                                                                                                                                           |
| GANCHO \_ TCXO<br/>                    | TCXO \_ PREHOOK \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | Combina a funcionalidade de pré-gancho e pós-gancho.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITablet Interface**](itablet.md)
</dt> <dt>

[**ENUMERAÇÃO \_ CONTEXT ENABLE \_ TYPE**](context-enable-type.md)
</dt> <dt>

[**Estrutura de configurações de \_ contexto do Tablet \_**](tablet-context-settings.md)
</dt> <dt>

[**Estrutura de descrição do pacote \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




