---
description: Cria um objeto de contexto que descreve o dispositivo tablet especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'Método ITablet:: CreateContext'
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
# <a name="itabletcreatecontext-method"></a>Método ITablet:: CreateContext

Cria um objeto de contexto que descreve o dispositivo tablet especificado.

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

*HWND* \[ no\]
</dt> <dd>

A janela à qual o contexto do Tablet será anexado.

</dd> <dt>

*prcInput* \[ no\]
</dt> <dd>

\[em, exclusivo\]

O retângulo de entrada à tinta.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Sinalizadores que definem opções de contexto do Tablet.

</dd> <dt>

*pTCS* \[ no\]
</dt> <dd>

\[em, exclusivo\]

Informações detalhadas sobre o contexto do Tablet a ser criado.

</dd> <dt>

*CET* \[ no\]
</dt> <dd>

Valor que habilita ou desabilita as mensagens de contexto que estão sendo enviadas para a janela.

</dd> <dt>

*ppCtx* \[ fora\]
</dt> <dd>

Um ponteiro para o novo contexto do Tablet.

</dd> <dt>

*pTcid* \[ entrada, saída\]
</dt> <dd>

Valor que identifica exclusivamente o Tablet.

</dd> <dt>

*ppPD* \[ entrada, saída\]
</dt> <dd>

Ponteiro para informações sobre quais dados estão contidos em cada pacote.

</dd> <dt>

*pSink* \[ no\]
</dt> <dd>

O objeto [**ITabletEventSink**](itableteventsink.md) em que as mensagens de notificação serão enviadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo obtém os valores padrão do [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica os valores para atender às suas necessidades e, em seguida, passa a estrutura de configurações modificada para o **método ITablet:: CreateContext**.

> [!Note]  
> Você deve implementar a [**interface ITabletEventSink**](itableteventsink.md) ao chamar o **método ITablet:: CreateContext**.

 

O parâmetro *dwOptions* é um conjunto de sinalizadores de bits que descrevem as opções de contexto. A tabela a seguir descreve esses sinalizadores.



| Nome do sinalizador                                | Valor                                                                                                                                                                                         | Descrição                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| margem de TCXO \_<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Especifica que o contexto de entrada no Tablet terá uma margem. A margem é uma área fora da área de entrada especificada, na qual os eventos serão mapeados para a borda da área de entrada. Esse recurso facilita a entrada de pontos na borda do contexto.<br/> |
| prehook TCXO \_<br/>                 | 0x00000002<br/>                                                                                                                                                                         | O prehook Obtém pacotes antes de contextos e de conganchos regulares. Eles obtêm pacotes na ordem de sua criação.<br/>                                                                                                                                                  |
| \_estado do cursor TCXO \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | O TC retornará pacotes, mesmo se o cursor estiver ativo. Por padrão, um TC retornará apenas os pacotes quando o cursor estiver inativo.<br/>                                                                                                                                       |
| TCXO \_ sem \_ cursor \_<br/>        | 0x00000008<br/>                                                                                                                                                                         | O TC não retornará pacotes quando o cursor estiver inativo.<br/>                                                                                                                                                                                                       |
| TCXO \_ não \_ integrado<br/>         | 0x00000010<br/>                                                                                                                                                                         | O contexto será não integrado.<br/>                                                                                                                                                                                                                           |
| TCXO \_<br/>                | 0x00000020<br/>                                                                                                                                                                         | O createhook Obtém pacotes após contextos de Tablet regulares, mas antes do contexto do sistema. Eles obtêm pacotes na ordem inversa de sua criação.<br/>                                                                                                                   |
| TCXO \_ não \_ Mostrar \_ cursor<br/>      | 0x00000080<br/>                                                                                                                                                                         | O TC não definirá a posição do cursor.<br/>                                                                                                                                                                                                                      |
| TCXO \_ não \_ validar \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | O TC não validará os GUIDs passados nas configurações de contexto do Tablet nas propriedades com suporte do dispositivo.<br/>                                                                                                                                      |
| TCXO \_ permitir \_ movimentos<br/>           | 0x00000400<br/>                                                                                                                                                                         | o TC permitirá que a detecção de movimento ocorra (por padrão, isso só é permitido em contextos do sistema) e o cliente receberá ES \_ eventos de movimento.<br/>                                                                                                               |
| TCXO \_ permitir \_ toques de comentários \_<br/>   | 0x00000800<br/>                                                                                                                                                                         | O TC permitirá que os comentários da caneta sejam mostrados. Por padrão, isso só é permitido em contextos do sistema.<br/>                                                                                                                                                              |
| TCXO \_ permitir \_ \_ desroscar comentários<br/> | 0x00001000<br/>                                                                                                                                                                         | O TC permitirá que os comentários da caneta sejam mostrados. Por padrão, isso só é permitido em contextos do sistema.<br/>                                                                                                                                                              |
| TCXO \_ tudo<br/>                     | TCXO \_ Margin \| TCXO pré- \_ gancho \| TCXO \_ estado do cursor \_ \| TCXO \_ não há \_ cursor \_ para baixo \| TCXO não integrado TCXO pré-Hook TCXO \_ não \_ \| \_ \| \_ \_ Mostrar \_ cursor TCXO não \| \_ \_ validar \_ TCS<br/> | Todas as opções de contexto do Tablet definidas.<br/>                                                                                                                                                                                                                           |
| gancho de TCXO \_<br/>                    | TCXO de TCXO de prehook \_ \| \_<br/>                                                                                                                                                    | Combina a funcionalidade de pré e pós-gancho.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> <dt>

[**\_Enumeração de tipo de habilitação de contexto \_**](context-enable-type.md)
</dt> <dt>

[**Estrutura de configurações de \_ contexto do Tablet \_**](tablet-context-settings.md)
</dt> <dt>

[**Estrutura de descrição do pacote \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




