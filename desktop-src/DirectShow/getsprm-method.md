---
description: O método GetSPRM recupera o registro de parâmetro do sistema especificado.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Método GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919703"
---
# <a name="getsprm-method"></a>Método GetSPRM

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetSPRM` método recupera o registro de parâmetro do sistema especificado.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica o registro cujo valor você deseja recuperar como um inteiro. O número inteiro deve variar de 0 a 23.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o conteúdo do registro especificado.

## <a name="remarks"></a>Comentários

O disco controla os registros de parâmetro do sistema (SPRMs). Um aplicativo de Player não precisa acessar esses registros para qualquer funcionalidade de navegação padrão. SPRMs representa o status do Player. Cada um tem um significado, definido por preferências do usuário, comandos de disco e outras ocorrências das quais um aplicativo não tem controle direto. Um aplicativo pode ler esses registros, mas não pode gravar neles. Para usar esses registros com eficiência, você provavelmente precisará de um conhecimento mais detalhado dos comandos de navegação do DVD do que é fornecido nesta documentação. A tabela a seguir mostra o conteúdo de cada registro. Para obter informações mais detalhadas sobre o conteúdo do registro, consulte [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registre-se | Sumário                        |
|----------|---------------------------------|
| 0        | Código de idioma do menu              |
| 1        | Número do fluxo de áudio             |
| 2        | Número de fluxo da subimagem        |
| 3        | Número do ângulo atual            |
| 4        | Número do título atual            |
| 5        | Número do título                    |
| 6        | Número de PGC                      |
| 7        | Número do capítulo atual (PTT)    |
| 8        | Número do botão realçado       |
| 9        | Temporizador de navegação                |
| 10       | Salto de PGC para navegação. temporizador         |
| 11       | Modo de apresentação de áudio do karaokê |
| 12       | Código de país/região do PML         |
| 13       | PML                             |
| 14       | Configuração de vídeo                   |
| 15       | Funcionalidade de áudio                |
| 16       | Idioma do áudio                  |
| 17       | Extensão de idioma de áudio        |
| 18       | Idioma da subimagem             |
| 19       | Extensão da linguagem de subimagem   |
| 20       | Código de região do Player              |
| 21       | Reservado                        |
| 22       | Reservado                        |
| 23       | Reservado                        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



