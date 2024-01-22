# Detecção de conflitos em redes IoT no Maude
Este repositório é contém a minha implementação no maude de uma rede de dispositivos simples IoT.
O arquivo `basic-sorts.maude` contém todos os arquivos necessários para a construção de uma rede.

Os arquivos `network-config-*.maude` contém diferentes configurações de rede. \
O arquivo `network-config-1.maude` contém a rede original, conforme especificada no trabalho. \
O arquivo `network-config-2.maude` contém uma rede com nenhum dispositivo configurado, a rede não faz nada. O esperado é haver um conflito devido à temperatura que aumentou demais. \
O arquivo `network-config-3.maude` contém uma rede com somente o ar condicionado configurado. O esperado é haver um conflito por esfriar demais ou ficar escuro demais. \
O arquivo `network-config-4.maude` contém uma rede com 2 ações contraditórias quando a temperatura atinge 25ºC. O esperado é haver um conflito direto no ar condicionado. \
O arquivo `network-config-5.maude` contém uma rede, mas sem a variável `ForçarLuzesDesligadas` configurada. O esperado haver um conflito pelo quarto estar claro durante a noite. \

Para uma visualizar o resultado de uma configuração, execute o seguinte comando: \
`./maude basic-sorts.maude network-config-*.maude`